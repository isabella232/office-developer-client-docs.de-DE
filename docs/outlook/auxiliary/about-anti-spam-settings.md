---
title: Informationen zu Anti-Spam-Einstellungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook können Benutzer Einstellungen für jedes Konto angeben, um das Konto vor Spam zu schützen. Solche Antispameinstellungen werden in einem Abschnitt gespeichert, der für dieses Konto im Benutzerprofil festgelegt ist.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316961"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="bf1db-104">Informationen zu Anti-Spam-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bf1db-104">About anti-spam settings</span></span>

<span data-ttu-id="bf1db-105">Outlook können Benutzer Einstellungen für jedes Konto angeben, um das Konto vor Spam zu schützen.</span><span class="sxs-lookup"><span data-stu-id="bf1db-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="bf1db-106">Solche Antispameinstellungen werden in einem Abschnitt gespeichert, der für dieses Konto im Benutzerprofil festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bf1db-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="bf1db-107">Verwenden Sie [die PROP_ACCT_PREFERENCES_UID-Eigenschaft,](prop_acct_preferences_uid.md) um die eindeutige ID (UID) für den Abschnitt im Profil zu erhalten, in dem die Einstellungen des Benutzers für dieses Konto gespeichert sind, einschließlich der Antispameinstellungen.</span><span class="sxs-lookup"><span data-stu-id="bf1db-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="bf1db-108">Verwenden Sie die folgenden Eigenschaften, um Antispameinstellungen für das Konto zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bf1db-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="bf1db-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als blockierte Absender für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bf1db-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="bf1db-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)– Gibt die Spamfilterungsstufe an, die der Benutzer für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bf1db-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="bf1db-111">In der folgenden Tabelle sind die unterstützten Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf1db-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="bf1db-112">Unterstützter Wert</span><span class="sxs-lookup"><span data-stu-id="bf1db-112">Supported value</span></span> |<span data-ttu-id="bf1db-113">Definition</span><span class="sxs-lookup"><span data-stu-id="bf1db-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="bf1db-114">Keine</span><span class="sxs-lookup"><span data-stu-id="bf1db-114">None</span></span>  <br/> |<span data-ttu-id="bf1db-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="bf1db-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="bf1db-116">Niedrig</span><span class="sxs-lookup"><span data-stu-id="bf1db-116">Low</span></span>  <br/> |<span data-ttu-id="bf1db-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="bf1db-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="bf1db-118">Mittel</span><span class="sxs-lookup"><span data-stu-id="bf1db-118">Medium</span></span>  <br/> |<span data-ttu-id="bf1db-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="bf1db-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="bf1db-120">Hoch</span><span class="sxs-lookup"><span data-stu-id="bf1db-120">High</span></span>  <br/> |<span data-ttu-id="bf1db-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bf1db-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="bf1db-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als vertrauenswürdige Empfänger für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bf1db-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="bf1db-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)– Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen und Domänen an, die der Benutzer als vertrauenswürdige Absender für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bf1db-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf1db-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf1db-124">See also</span></span>

- [<span data-ttu-id="bf1db-125">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="bf1db-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="bf1db-126">Hinzufügen von Namen zu junk-E-Mail-Filterlisten</span><span class="sxs-lookup"><span data-stu-id="bf1db-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

