---
title: Kanonische PidTagExchangeProfileSectionId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316429"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="8e2a5-103">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e2a5-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="8e2a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e2a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e2a5-105">Enthält eine dynamisch generierte GUID, mit der ein Konto ermittelt wird, wenn Sie mehrere Microsoft Exchange Server-Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e2a5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8e2a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e2a5-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="8e2a5-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="8e2a5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8e2a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e2a5-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="8e2a5-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="8e2a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8e2a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e2a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e2a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e2a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8e2a5-112">Area:</span></span>  <br/> |<span data-ttu-id="8e2a5-113">Mehrere Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="8e2a5-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e2a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e2a5-114">Remarks</span></span>

<span data-ttu-id="8e2a5-115">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrere Exchange-Konten anstelle eines einzelnen Exchange-Kontos.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="8e2a5-116">Zur Unterstützung mehrerer Exchange-Konten wurde das MAPI-Profil Layout geändert.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="8e2a5-117">In Microsoft Office Outlook 2007 und früheren Versionen enthielten Profile einen Abschnitt mit festen Profilen für Exchange-Einstellungen wie Servername, Benutzername und Offline Ordner Datei (Ost).</span><span class="sxs-lookup"><span data-stu-id="8e2a5-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="8e2a5-118">Lage.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-118">location.</span></span> <span data-ttu-id="8e2a5-119">Diese Einstellungen wurden mithilfe eines eindeutigen Bezeichners, der **pbglobalprofilesectionguidabgerufen** -Eigenschaft, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="8e2a5-120">Der für Exchange-Einstellungen verwendete Abschnitt wird als Abschnitt Exchange Global profile bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="8e2a5-121">Ein fester Profil Abschnitts Speicherort ist nicht mehr ausreichend, um mehrere Exchange-Konten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="8e2a5-122">Stattdessen ist für jedes Exchange-Konto in Ihrem Profil ein Abschnitt vorhanden, der den Einstellungen für dieses Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="8e2a5-123">Der neue Abschnitt für Exchange-Einstellungen wird durch die eindeutige ID **emsmdbUID**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="8e2a5-124">Im Abschnitt Nachrichtendienst Profil für das Exchange-Konto finden Sie eine Eigenschaft, die eine GUID enthält, die zum Zeitpunkt der Erstellung des Kontos dynamisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="8e2a5-125">Diese GUID wird in der **PidTagExchangeProfileSectionId** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="8e2a5-126">Nachrichtenspeicher und Adressbuchcontainer stellen eine Eigenschaft bereit, um zu bestimmen, zu welchem Exchange-Konto Sie gehören.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="8e2a5-127">In der Tabelle Nachrichtendienste verfügbar, macht jeder Exchange-Dienst diese Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="8e2a5-128">Sie können diese Eigenschaft über einen Aufruf von [IMAPIProp::](imapiprop-getprops.md) getpropes auf **PidTagExchangeProfileSectionId** abrufen, nachdem Sie eine der folgenden Schnittstellen abgefragt haben:</span><span class="sxs-lookup"><span data-stu-id="8e2a5-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="8e2a5-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e2a5-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="8e2a5-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8e2a5-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="8e2a5-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8e2a5-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="8e2a5-132">Wenn das Objekt nicht mit Exchange verbunden ist, gibt der Aufruf **MAPI_E_NOT_FOUND**zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="8e2a5-133">Sie können Container für eine **PidTagExchangeProfileSectionId** einschränken, wenn das Adressbuch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="8e2a5-134">Sobald Sie über einen geöffneten Container verfügen, können Sie den **emsmdbUID** davon Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="8e2a5-135">Außerdem sollte beachtet werden, dass ein Empfänger, der aus einem Exchange-Adressbuch ausgewählt wurde, auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e2a5-136">In den Codebeispielen und Funktions Kopfzeilen wird diese GUID als **emsmdbUID**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="8e2a5-137">Eines der Exchange-Konten ist als Legacy-Exchange-Konto gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="8e2a5-138">NormalerWeise ist es das erste Konto, das dem Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="8e2a5-139">Jeder Aufruf von Open **pbglobalprofilesectionguidabgerufen** wird an den Abschnitt Exchange Global des Legacy Kontos umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="8e2a5-140">Die Objektmodellaufrufe, die mit dem Exchange-Konto nicht Legacy interagieren, interagieren auch mit dem Legacy-Exchange-Konto.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="8e2a5-141">Der Exchange-Legacy Dienst hat die Eigenschaft **PR_EMSMDB_LEGACY** (0x3D18000B), die in der Tabelle Nachrichtendienste auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="8e2a5-142">Das Legacy- **emsmdbUID** wird auch im Abschnitt Outlook Global Profile des Profils als **PidTagExchangeProfileSectionId**gestempelt.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="8e2a5-143">Code, der zur Unterstützung mehrerer Exchange-Konten geschrieben wurde, sollte nicht den Legacy- **emsmdbUID** abrufen müssen, da er die richtige **emsmdbUID**erhalten soll, je nachdem, mit welchem Konto Ihr Code interagiert.</span><span class="sxs-lookup"><span data-stu-id="8e2a5-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e2a5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e2a5-144">See also</span></span>



[<span data-ttu-id="8e2a5-145">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="8e2a5-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="8e2a5-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="8e2a5-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

