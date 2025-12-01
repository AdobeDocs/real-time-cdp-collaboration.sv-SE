---
title: Konfigurera AWS-behörigheter för målgruppskälla
description: Lär dig hur du konfigurerar behörigheter för AWS Identity and Access Management (IAM) för att ge Adobe säker, skrivskyddad åtkomst till din [!DNL Amazon S3] bucket för målgruppskälla i Real-Time CDP Collaboration.
source-git-commit: 73f11b7341cf94540dc01f8803291f6dc3cd5038
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Konfigurera AWS-behörigheter för målgruppskälla

Använd den här guiden för att konfigurera principer och roller för AWS Identity and Access Management (IAM) som ger Adobe säker, skrivskyddad åtkomst till ditt Amazon S3-paket. Med den här åtkomsten kan Real-Time CDP Collaboration hämta målgrupper från er S3-bucket.

## Förhandskrav {#prerequisites}

Innan du fortsätter bör du kontrollera att du uppfyller följande krav och har tillgång till den information som krävs.

### Nödvändiga AWS-behörigheter

För att slutföra den här konfigurationen måste ditt konto ha AWS administratörsåtkomst. Administratörsåtkomst säkerställer att du kan skapa och hantera IAM-profiler och roller som krävs för att godkänna Adobe åtkomst till din S3-bucket. Om du inte har administratörsbehörighet kontaktar du AWS-administratören innan du fortsätter.

### Nödvändig information

Observera följande när du går igenom stegen nedan. De här detaljerna används i [[!DNL Amazon S3] användargränssnittsguiden för målgruppskälla](./configure-aws-s3-audience-sourcing.md).

* Namnet på S3-bucket där målgruppsfilerna lagras.
* Mappsökvägen (prefix) under vilken målgruppsfilerna finns.
* Amazon Resource Name (ARN) för din nyligen skapade IAM-roll, till exempel: `arn:aws:s3:::my-company-data/audience-files/`

>[!TIP]
>
>Ett Amazon Resource Name (ARN) är en unik identifiering av AWS-resurser, som S3-bucket och IAM-roller. Använd följande format för att ange din bucket och valfri mappsökväg:
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Skapa en IAM-princip {#create-policy}

Börja med att skapa en IAM-princip som ger **skrivskyddad åtkomst** till din S3-bucket för att starta konfigurationen. Med den här principen kan Adobe läsa de filer som behövs för målgruppskälla, men inte bevilja skriv- eller borttagningsbehörigheter.

Öppna [AWS Management Console](https://aws.amazon.com/console/) och gå till **[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**.

På arbetsytan för AWS Create policy väljer du fliken **JSON** och klistrar in följande exempelprincip.

>[!NOTE]
>
>Ersätt `<Your AWS ARN for bucket folder path>` och `<Your AWS ARN for bucket>` med dina specifika S3 ARN:er. När du anger sökvägen till bucket-mappen tar du med `/*` i slutet av ARN (till exempel `arn:aws:s3:::my-company-data/audience-files/*`). Detta garanterar att Adobe har tillgång till alla filer och undermappar i den angivna mappsökvägen.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "<Your AWS ARN for bucket folder path>"
    },
    {
      "Sid": "Statement2",
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "<Your AWS ARN for bucket>"
    }
  ]
}
```

Granska principinställningarna och välj **[!DNL Create policy]**. Registrera principnamnet som ska användas i ett senare steg.

>[!TIP]
>
>Öppna **Amazon S3 Management Console** om du vill hitta ditt bucketnamn och din mappsökväg. På sidan **Bucket** väljer du ditt bucket-namn för att öppna den. I vyn **Objekt** visas dina filer och mappar. Sökvägen högst upp på sidan visar din aktuella mappsökväg.

## Skapa en IAM-roll {#create-role}

Skapa sedan en IAM-roll och ange Real-Time CDP Collaboration AWS IAM-rollen som **betrodd entitet**. Detta gör att Adobe tjänster kan ta sig an rollen och läsa era målgruppsdata i S3 på ett säkert sätt.

Gå till **[!DNL IAM]** > **[!DNL Roles]** på fliken **[!DNL Create role]** i Amazon S3 Management Console.

Under [!DNL Step 1] i [!DNL Create role]-arbetsflödet väljer du **[!DNL Trusted entity type]** i avsnittet **[!DNL Custom trust policy]**. Klistra sedan in följande exempel i **[!DNL Custom trust policy]**-redigeraren och ersätt `<Adobe IAM Role ARN>` med värdet för din region.

* Adobe IAM Role ARN:

| Län | Adobe IAM Role ARN |
|---------|-------------------|
| Nordamerika | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australien | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

Ett exempel på förtroendeprincip:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "<Adobe IAM Role ARN>"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

Granska profilen och välj **Nästa** för att fortsätta.

I avsnittet [!DNL Step 2] **[!DNL Add permissions]** i arbetsflödet [!DNL Create role] söker du efter och bifogar IAM-principen som du skapade [tidigare](#create-policy). Välj principen som följs av **[!DNL Next]** för att fortsätta till [!DNL Step 3].

I avsnittet [!DNL Step 3] **[!DNL Name review, and create - Role details]** anger du ett rollnamn (till exempel `s3-iam-role`) och en valfri beskrivning.

På den här sidan visas den betrodda entitetsprincipen, sammanfattningen av behörighetsprinciper och eventuella taggar som du har lagt till för intern organisation och spårning.

Slutligen väljer du **Skapa roll** för att bekräfta konfigurationen.

>[!IMPORTANT]
>
>Du måste registrera Amazon Resource Name (ARN) när du har skapat rollen. Du måste ange IAM-rollens ARN under steget **Verifiera din S3-anslutning** i arbetsflödet [Konfigurera AWS S3 för målgruppskälla](./configure-aws-s3-audience-sourcing.md).

## Nästa steg {#next-steps}

Den här installationen ger Adobe skrivskyddad åtkomst till din S3-bucket och upprättar en betrodd anslutning med Adobe IAM-roll.

Fortsätt sedan till [Konfigurera AWS S3 för målgruppskälla](./configure-aws-s3-audience-sourcing.md) för att ansluta S3-bucket till Collaboration.

Mer information om att hämta målgrupper finns i [Source och hantera målgrupper](./onboard-audiences.md).
