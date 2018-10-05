---
title: Informationen zum Registrieren von Stores für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386530"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="88335-103">Informationen zum Registrieren von Stores für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="88335-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="88335-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88335-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88335-105">In diesem Thema wird speziell für die Sofortsuche in Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="88335-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="88335-106">Sofortsuche können Sie die Elemente in Outlook schnell finden.</span><span class="sxs-lookup"><span data-stu-id="88335-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="88335-107">Komponenten der Windows-Desktopsuche verwendet.</span><span class="sxs-lookup"><span data-stu-id="88335-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="88335-108">Der MAPI-Protokollhandler überprüft die Windows-Registrierung für Geschäfte, die indiziert werden soll für die Suche.</span><span class="sxs-lookup"><span data-stu-id="88335-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="88335-109">Speicheranbieter, die indiziert werden soll, müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="88335-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="88335-110">Standardmäßig wird der Windows-Registrierung zu indizieren mit Windows-Desktopsuche die folgenden vier Typen von Anbietern hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="88335-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="88335-111">Speicher für Persönliche Ordner-Dateien (. PST).</span><span class="sxs-lookup"><span data-stu-id="88335-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="88335-112">Microsoft Exchange-Speicher, einschließlich alle Offlineordnerdateien (OST).</span><span class="sxs-lookup"><span data-stu-id="88335-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="88335-113">Informationsspeicher für Öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="88335-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="88335-114">Anmelden für Microsoft Office Outlook Connector für MSN.</span><span class="sxs-lookup"><span data-stu-id="88335-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="88335-115">Drittanbieter-Anbieter, die indiziert werden möchten, müssen sich selbst in der Windows-Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="88335-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="88335-116">Administratoren und Benutzer können eine Gruppenrichtlinie verwenden, um zu verhindern, dass Windows-Desktopsuche Indizieren von Outlook-Elementen.</span><span class="sxs-lookup"><span data-stu-id="88335-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="88335-117">Weitere Informationen finden Sie unter [Windows-Desktopsuche erweitern](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="88335-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="88335-118">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="88335-118">Registry Keys</span></span>

<span data-ttu-id="88335-119">Auf einem Computer müssen alle Speicher-Anbieter, die indiziert werden soll, unter nur einer der folgenden drei Registrierungsschlüssel in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="88335-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="88335-120">Der MAPI-Protokollhandler sieht unter jeder dieser Schlüssel in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="88335-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="88335-121">\Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="88335-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="88335-122">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="88335-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="88335-123">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]</span><span class="sxs-lookup"><span data-stu-id="88335-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="88335-124">Jeder Wert unter dem Schlüssel entspricht einem Anbieter, der indiziert werden würde.</span><span class="sxs-lookup"><span data-stu-id="88335-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="88335-125">Der Name des Werts ist die GUID (GLOBALLY Unique Identifier) des Anbieters, die vom Typ **DWORD-Wert** und den Hexadezimalwert 0 x 00000001 hat.</span><span class="sxs-lookup"><span data-stu-id="88335-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="88335-126">GUIDs für Anbieter</span><span class="sxs-lookup"><span data-stu-id="88335-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="88335-127">Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID der MAPI-Speicher.</span><span class="sxs-lookup"><span data-stu-id="88335-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="88335-128">Die GUIDs für den Anbieter, dass Outlook Indizes in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="88335-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="88335-129">**Typ des Anbieters**</span><span class="sxs-lookup"><span data-stu-id="88335-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="88335-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="88335-130">**GUID**</span></span> <br/> |<span data-ttu-id="88335-131">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="88335-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="88335-132">Persönliche Ordner-Dateien (. PST)</span><span class="sxs-lookup"><span data-stu-id="88335-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="88335-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="88335-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="88335-134">GUID wird in der öffentlichen Header Datei mspst.h als **MSPST_UID_PROVIDER** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="88335-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="88335-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="88335-135">Exchange</span></span>  <br/> |<span data-ttu-id="88335-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="88335-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="88335-137">GUID wird in der öffentlichen Header Datei edkmdb.h als **PbExchangeProviderPrimaryUserGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="88335-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="88335-138">Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="88335-138">Public folders</span></span>  <br/> |<span data-ttu-id="88335-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="88335-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="88335-140">GUID wird in der öffentlichen Header Datei edkmdb.h als **PbExchangeProviderPublicGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="88335-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="88335-141">Outlook Connector für MSN</span><span class="sxs-lookup"><span data-stu-id="88335-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="88335-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="88335-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="88335-143">Keine</span><span class="sxs-lookup"><span data-stu-id="88335-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88335-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88335-144">See also</span></span>



[<span data-ttu-id="88335-145">Informationen zur Store-API</span><span class="sxs-lookup"><span data-stu-id="88335-145">About the Store API</span></span>](about-the-store-api.md)

