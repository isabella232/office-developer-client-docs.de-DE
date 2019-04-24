---
title: Informationen zum Registrieren von Speichern für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321826"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="d9cb0-103">Informationen zum Registrieren von Speichern für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="d9cb0-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="d9cb0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9cb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9cb0-105">Dieses Thema ist speziell für die Sofortsuche in Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="d9cb0-106">Mit der Sofortsuche können Sie Elemente in Outlook schnell finden.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="d9cb0-107">Es werden Komponenten der Windows-Desktop Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="d9cb0-108">Der MAPI-Protokoll Handler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="d9cb0-109">Speicheranbieter, die indiziert werden sollen, müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="d9cb0-110">Standardmäßig werden von der Windows-Desktop Suche die folgenden vier Typen von Speicheranbietern zur Windows-Registrierung hinzugefügt, um die Indizierung zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="d9cb0-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="d9cb0-111">Speicher für persönliche Ordner-Dateien (. PST).</span><span class="sxs-lookup"><span data-stu-id="d9cb0-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="d9cb0-112">Microsoft Exchange-Speicher, einschließlich aller Offline Ordner Dateien (Ost).</span><span class="sxs-lookup"><span data-stu-id="d9cb0-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="d9cb0-113">Speicher für Öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="d9cb0-114">Store für Microsoft Office Outlook Connector für MSN.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="d9cb0-115">Drittanbieter-Speicheranbieter, die indiziert werden sollen, müssen sich in der Windows-Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d9cb0-116">Administratoren und Benutzer können eine Gruppenrichtlinieneinstellung verwenden, um zu verhindern, dass die Windows-Desktop Suche Outlook-Elemente indiziert.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="d9cb0-117">Weitere Informationen finden Sie unter [Erweitern der Windows-Desktop Suche](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d9cb0-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="d9cb0-118">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d9cb0-118">Registry Keys</span></span>

<span data-ttu-id="d9cb0-119">Auf einem Computer müssen alle Speicheranbieter, die indiziert werden sollen, unter nur einem der folgenden drei Registrierungsschlüssel in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="d9cb0-120">Der MAPI-Protokoll Handler sieht unter jedem dieser Schlüssel in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="d9cb0-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="d9cb0-121">[HKLM] \Software\Policies\Microsoft\Windows\Windows-Suche \\</span><span class="sxs-lookup"><span data-stu-id="d9cb0-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="d9cb0-122">[HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="d9cb0-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="d9cb0-123">[HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="d9cb0-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="d9cb0-124">Jeder Wert unter dem Schlüssel entspricht einem Speicheranbieter, der indiziert werden würde.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="d9cb0-125">Der Name des Werts ist die GUID (Globally Unique Identifier) des Speicheranbieters, der vom Typ **DWORD** ist und den Hexadezimalwert 0x00000001 aufweist.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="d9cb0-126">GUIDs für Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="d9cb0-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="d9cb0-127">Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID eines MAPI-Speichers an.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="d9cb0-128">Die GUIDs für die Informationsspeicher Anbieter, die Outlook-Indizes in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d9cb0-129">**Typ des Speicheranbieters**</span><span class="sxs-lookup"><span data-stu-id="d9cb0-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="d9cb0-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="d9cb0-130">**GUID**</span></span> <br/> |<span data-ttu-id="d9cb0-131">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="d9cb0-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="d9cb0-132">Persönliche Ordner-Dateien (. PST</span><span class="sxs-lookup"><span data-stu-id="d9cb0-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="d9cb0-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="d9cb0-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="d9cb0-134">Die GUID ist in der öffentlichen Headerdatei MSPST. h als **MSPST_UID_PROVIDER** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="d9cb0-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="d9cb0-135">Exchange</span></span>  <br/> |<span data-ttu-id="d9cb0-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="d9cb0-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="d9cb0-137">Die GUID ist in der öffentlichen Headerdatei edkmdb. h als **pbExchangeProviderPrimaryUserGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="d9cb0-138">Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="d9cb0-138">Public folders</span></span>  <br/> |<span data-ttu-id="d9cb0-139">{70fab278-f7af-CD11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="d9cb0-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="d9cb0-140">Die GUID ist in der öffentlichen Headerdatei edkmdb. h als **pbExchangeProviderPublicGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d9cb0-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="d9cb0-141">Outlook Connector für MSN</span><span class="sxs-lookup"><span data-stu-id="d9cb0-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="d9cb0-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="d9cb0-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="d9cb0-143">Keine</span><span class="sxs-lookup"><span data-stu-id="d9cb0-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9cb0-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9cb0-144">See also</span></span>



[<span data-ttu-id="d9cb0-145">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="d9cb0-145">About the Store API</span></span>](about-the-store-api.md)

