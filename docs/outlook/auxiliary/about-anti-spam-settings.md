---
title: Informationen zu Anti-Spam-Einstellungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook ermöglicht Benutzern das Angeben von Einstellungen für jedes Konto das Konto vor Spam schützen. Eine solche Anti-Spam-Dateien werden in einem Abschnitt vorgesehen für dieses Konto im Profil des Benutzers gespeichert.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790910"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="405e7-104">Informationen zu Anti-Spam-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="405e7-104">About anti-spam settings</span></span>

<span data-ttu-id="405e7-105">Outlook ermöglicht Benutzern das Angeben von Einstellungen für jedes Konto das Konto vor Spam schützen.</span><span class="sxs-lookup"><span data-stu-id="405e7-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="405e7-106">Eine solche Anti-Spam-Dateien werden in einem Abschnitt vorgesehen für dieses Konto im Profil des Benutzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="405e7-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="405e7-107">Verwenden Sie die [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) -Eigenschaft, um die eindeutige ID (UID) für den Abschnitt im Profil abzurufen, die Einstellungen für dieses Konto, einschließlich der Anti-Spam-Einstellungen des Benutzers gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="405e7-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="405e7-108">Verwenden Sie die folgenden Eigenschaften, um Anti-Spam-Einstellungen für das Konto abzurufen:</span><span class="sxs-lookup"><span data-stu-id="405e7-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="405e7-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die der Benutzer als geblockten Absender für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="405e7-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="405e7-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)– gibt die Ebene der Spam-filtern, die der Benutzer für das Konto angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="405e7-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="405e7-111">In der folgenden Tabelle sind die unterstützten Werte.</span><span class="sxs-lookup"><span data-stu-id="405e7-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="405e7-112">Unterstützte Wert</span><span class="sxs-lookup"><span data-stu-id="405e7-112">Supported value</span></span> |<span data-ttu-id="405e7-113">Definition</span><span class="sxs-lookup"><span data-stu-id="405e7-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="405e7-114">Keine</span><span class="sxs-lookup"><span data-stu-id="405e7-114">None</span></span>  <br/> |<span data-ttu-id="405e7-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="405e7-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="405e7-116">Low</span><span class="sxs-lookup"><span data-stu-id="405e7-116">Low</span></span>  <br/> |<span data-ttu-id="405e7-117">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="405e7-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="405e7-118">Medium</span><span class="sxs-lookup"><span data-stu-id="405e7-118">Medium</span></span>  <br/> |<span data-ttu-id="405e7-119">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="405e7-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="405e7-120">High</span><span class="sxs-lookup"><span data-stu-id="405e7-120">High</span></span>  <br/> |<span data-ttu-id="405e7-121">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="405e7-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="405e7-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die als vertrauenswürdige Empfänger für das Konto der Benutzer angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="405e7-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="405e7-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)– gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen und Domänen, die als vertrauenswürdige Absender für das Konto der Benutzer angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="405e7-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="405e7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="405e7-124">See also</span></span>

- [<span data-ttu-id="405e7-125">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="405e7-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="405e7-126">Hinzufügen von Namen zu den Listen Junk-e-Mail-Filter</span><span class="sxs-lookup"><span data-stu-id="405e7-126">Add names to the Junk Email Filter lists</span></span>](http://office.microsoft.com/de-de/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

