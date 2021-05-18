---
title: PidTagExchangeProfileSectionId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316429"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="1a019-103">PidTagExchangeProfileSectionId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1a019-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="1a019-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a019-105">Enthält eine dynamisch generierte GUID, die zum Bestimmen eines Kontos verwendet wird, wenn Sie mehrere Microsoft Exchange Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a019-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a019-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a019-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a019-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="1a019-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="1a019-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1a019-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a019-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="1a019-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="1a019-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a019-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a019-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a019-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a019-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a019-112">Area:</span></span>  <br/> |<span data-ttu-id="1a019-113">Mehrere Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="1a019-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a019-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a019-114">Remarks</span></span>

<span data-ttu-id="1a019-115">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrere Exchange konten anstelle eines Exchange Kontos.</span><span class="sxs-lookup"><span data-stu-id="1a019-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="1a019-116">Um mehrere Exchange zu verwenden, wurde das MAPI-Profillayout geändert.</span><span class="sxs-lookup"><span data-stu-id="1a019-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="1a019-117">In Microsoft Office Outlook 2007 und früheren Versionen enthielten Profile einen festen Profilabschnitt für Exchange-Einstellungen wie Servername, Benutzername und Offlineordnerdatei (OST).</span><span class="sxs-lookup"><span data-stu-id="1a019-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="1a019-118">speicherort.</span><span class="sxs-lookup"><span data-stu-id="1a019-118">location.</span></span> <span data-ttu-id="1a019-119">Diese Einstellungen wurden mithilfe eines eindeutigen Bezeichners identifiziert, der **pbGlobalProfileSectionGuid-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="1a019-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="1a019-120">Der abschnitt, der für Exchange einstellungen verwendet wird, wird als Exchange Global Profile Section bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a019-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="1a019-121">Ein fester Profilabschnittsspeicherort ist nicht mehr ausreichend, um mehrere Exchange aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="1a019-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="1a019-122">Stattdessen ist für jedes Exchange in Ihrem Profil ein Abschnitt vorhanden, der den Einstellungen für dieses Konto gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="1a019-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="1a019-123">Der neue Abschnitt, der für Exchange verwendet wird, wird durch den eindeutigen Bezeichner **emsmdbUID identifiziert.**</span><span class="sxs-lookup"><span data-stu-id="1a019-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="1a019-124">Im Abschnitt Nachrichtendienstprofil für das Exchange finden Sie eine Eigenschaft, die eine GUID enthält, die dynamisch generiert wird, wenn das Konto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1a019-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="1a019-125">Diese GUID wird in der **PidTagExchangeProfileSectionId-Eigenschaft** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1a019-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="1a019-126">Nachrichtenspeicher und Adressbuchcontainer machen eine Eigenschaft verfügbar, um zu bestimmen, Exchange sie gehören.</span><span class="sxs-lookup"><span data-stu-id="1a019-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="1a019-127">Auf den Zugriff in der Tabelle "Nachrichtendienste" kann Exchange diese Eigenschaft verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="1a019-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="1a019-128">Sie können diese Eigenschaft über einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) auf **PidTagExchangeProfileSectionId** abrufen, nachdem Sie eine der folgenden Schnittstellen abgefragt haben:</span><span class="sxs-lookup"><span data-stu-id="1a019-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="1a019-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1a019-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="1a019-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1a019-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="1a019-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1a019-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="1a019-132">Wenn das Objekt nicht mit einer Exchange verbunden ist, gibt der Aufruf **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="1a019-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="1a019-133">Sie können Container für eine **PidTagExchangeProfileSectionId** einschränken, wenn Sie das Adressbuch anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a019-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="1a019-134">Sobald Sie über einen geöffneten Container verfügen, können Sie **die emsmdbUID von** diesem abfragen.</span><span class="sxs-lookup"><span data-stu-id="1a019-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="1a019-135">Es ist auch erwähnenswert, dass der Empfänger auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften enthält, wenn ein Empfänger aus einem Exchange-Adressbuch ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a019-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1a019-136">In den Codebeispielen und Funktionskopfzeilen wird diese GUID als **emsmdbUID bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="1a019-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="1a019-137">Eines der Exchange wird als Legacykonto Exchange gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a019-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="1a019-138">In der Regel ist es das erste Konto, das dem Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a019-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="1a019-139">Jeder Aufruf zum Öffnen **von pbGlobalProfileSectionGuid** wird an den globalen Exchange des Legacykontos umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1a019-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="1a019-140">Das Objektmodell ruft Aufrufe auf, die mit dem Nicht-Legacy-Exchange interagieren, auch mit dem Legacykonto Exchange interagieren.</span><span class="sxs-lookup"><span data-stu-id="1a019-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="1a019-141">Der legacy Exchange-Dienst verfügt über **die Eigenschaft PR_EMSMDB_LEGACY** (0x3D18000B), die in der Nachrichtendiensttabelle auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1a019-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="1a019-142">Die ältere **emsmdbUID** wird auch im Abschnitt Outlook Global Profile des Profils als **PidTagExchangeProfileSectionId gestempelt.**</span><span class="sxs-lookup"><span data-stu-id="1a019-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="1a019-143">Code, der zur Unterstützung mehrerer Exchange-Konten geschrieben wurde, sollte nicht die ältere **emsmdbUID** abrufen, da er die richtige **emsmdbUID** abrufen sollte, abhängig vom Konto, mit dem Ihr Code interagiert.</span><span class="sxs-lookup"><span data-stu-id="1a019-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a019-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a019-144">See also</span></span>



[<span data-ttu-id="1a019-145">Verwenden mehrerer Exchange Konten</span><span class="sxs-lookup"><span data-stu-id="1a019-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="1a019-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="1a019-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

