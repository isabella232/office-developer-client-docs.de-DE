---
title: Informationen zum Registrieren von Speichern für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte Änderung: 9. März 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321826"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="29ac8-103">Informationen zum Registrieren von Speichern für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="29ac8-103">About registering stores for indexing</span></span>

  
  
<span data-ttu-id="29ac8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29ac8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29ac8-105">Dieses Thema gilt speziell für die Sofortsuche in Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="29ac8-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="29ac8-106">Mit der Sofortsuche können Sie Elemente in Outlook schnell auffinden.</span><span class="sxs-lookup"><span data-stu-id="29ac8-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="29ac8-107">Sie verwendet Komponenten der Windows-Desktopsuche.</span><span class="sxs-lookup"><span data-stu-id="29ac8-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="29ac8-108">Der MAPI-Protokollhandler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indizieren werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29ac8-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="29ac8-109">Speicheranbieter, die indiziert werden wollen, müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="29ac8-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="29ac8-110">Das Windows-Desktopsuche fügt standardmäßig die folgenden vier Arten von Speicheranbietern zur Windows-Registrierung hinzu, um die Indizierung zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="29ac8-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="29ac8-111">Speicher für persönliche Ordner-Dateien (PST)</span><span class="sxs-lookup"><span data-stu-id="29ac8-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="29ac8-112">Microsoft Exchange-Speicher, einschließlich aller Offlineordnerdateien (OST).</span><span class="sxs-lookup"><span data-stu-id="29ac8-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="29ac8-113">Speicher für öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="29ac8-113">Limits for public folders</span></span> 
    
-  <span data-ttu-id="29ac8-114">Speicher für Microsoft Office Outlook Connector für MSN.</span><span class="sxs-lookup"><span data-stu-id="29ac8-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="29ac8-115">Externe Speicheranbieter, die indiziert werden wollen, müssen sich in der Windows-Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="29ac8-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="29ac8-116">Administratoren und Benutzer können eine Gruppenrichtlinieneinstellung verwenden, um zu verhindern, dass die Windows-Desktopsuche Outlook-Elemente indiziert.</span><span class="sxs-lookup"><span data-stu-id="29ac8-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="29ac8-117">Weitere Informationen finden Sie unter [Erweitern der Windows-Desktopsuche](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="29ac8-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="29ac8-118">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="29ac8-118">Registry keys</span></span>

<span data-ttu-id="29ac8-119">Auf einem Computer müssen alle Speicheranbieter, die indiziert werden wollen, unter nur einem der folgenden drei Registrierungsschlüssel in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="29ac8-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="29ac8-120">Der MAPI-Protokollhandler sucht unter jedem dieser Schlüssel in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="29ac8-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="29ac8-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span><span class="sxs-lookup"><span data-stu-id="29ac8-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="29ac8-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="29ac8-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="29ac8-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="29ac8-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="29ac8-124">Jeder Wert unter dem Schlüssel entspricht einem Speicheranbieter, der indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="29ac8-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="29ac8-125">Der Name des Werts ist der Globally Unique Identifier (GUID) des Speicheranbieters, der vom Typ **DWORD** ist und den hexadezimalen Wert 0x00000001 aufweist.</span><span class="sxs-lookup"><span data-stu-id="29ac8-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="29ac8-126">GUIDs für Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="29ac8-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="29ac8-127">Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID eines MAPI-Speichers an.</span><span class="sxs-lookup"><span data-stu-id="29ac8-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="29ac8-128">Die GUIDs für die Speicheranbieter, die Outlook indiziert, sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="29ac8-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="29ac8-129">**Typ des Speicheranbieters**</span><span class="sxs-lookup"><span data-stu-id="29ac8-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="29ac8-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="29ac8-130">**GUID**</span></span> <br/> |<span data-ttu-id="29ac8-131">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="29ac8-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="29ac8-132">Persönliche Ordner-Dateien (PST)</span><span class="sxs-lookup"><span data-stu-id="29ac8-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="29ac8-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="29ac8-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="29ac8-134">Die GUID wird in der öffentlichen Headerdatei "mspst.h" als **MSPST_UID_PROVIDER** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="29ac8-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="29ac8-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="29ac8-135">Exchange</span></span>  <br/> |<span data-ttu-id="29ac8-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="29ac8-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="29ac8-137">Die GUID wird in der öffentlichen Headerdatei "edkmdb.h" als **pbExchangeProviderPrimaryUserGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="29ac8-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="29ac8-138">Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="29ac8-138">Public folders</span></span>  <br/> |<span data-ttu-id="29ac8-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="29ac8-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="29ac8-140">Die GUID wird in der öffentlichen Headerdatei "edkmdb.h" als **pbExchangeProviderPublicGuid** dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="29ac8-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="29ac8-141">Outlook-Connector für MSN</span><span class="sxs-lookup"><span data-stu-id="29ac8-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="29ac8-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="29ac8-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="29ac8-143">Keine</span><span class="sxs-lookup"><span data-stu-id="29ac8-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29ac8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ac8-144">See also</span></span>



[<span data-ttu-id="29ac8-145">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="29ac8-145">About the Store API</span></span>](about-the-store-api.md)

