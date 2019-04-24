---
title: PidTagFolderWebViewInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316310"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="4a5f2-103">PidTagFolderWebViewInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a5f2-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="4a5f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a5f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a5f2-105">Enthält die URL für die Startseite eines Ordners in Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="4a5f2-106">Diese Eigenschaft enthält einen binären Datenstromnamens **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a5f2-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a5f2-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a5f2-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="4a5f2-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="4a5f2-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4a5f2-109">Identifier:</span></span>  <br/> |<span data-ttu-id="4a5f2-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="4a5f2-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="4a5f2-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a5f2-111">Data type:</span></span>  <br/> |<span data-ttu-id="4a5f2-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a5f2-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a5f2-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a5f2-113">Area:</span></span>  <br/> |<span data-ttu-id="4a5f2-114">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="4a5f2-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a5f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a5f2-115">Remarks</span></span>

<span data-ttu-id="4a5f2-116">Für einen beliebigen Outlook-Ordner kann eine Homepage-URL angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="4a5f2-117">Auf diese Informationen kann in Outlook über die Registerkarte **Startseite** des Dialogfelds Eigenschaften für einen Ordner zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="4a5f2-118">Abhängig von bestimmten Richtlinieneinstellungen wird die Homepage möglicherweise von Outlook ignoriert, wenn der MAPI-Speicher, der diesen Ordner enthält, MSCAP_SECURE_FOLDER_HOMEPAGES nicht in seiner [IMSCapabilities:: getCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) -Implementierung meldet.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="4a5f2-119">Sowohl der **Outlook Heute** -Ordner als auch ein öffentlicher Ordner können URLs der Homepage enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="4a5f2-120">Der **Outlook Heute** -Ordner verwendet jedoch einen anderen Mechanismus, um die URL der Startseite zu verwalten. Dieser Mechanismus wird in diesem Thema nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="4a5f2-121">Ein öffentlicher Ordner kann auch eine für einen benutzerspezifische Homepage-URL enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="4a5f2-122">Diese Funktion wird jedoch in diesem Thema nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="4a5f2-123">Der Wert dieser Eigenschaft ist ein binärer Datenstromnamens **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="4a5f2-124">WebViewPersistenceObject-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="4a5f2-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="4a5f2-125">Die **WebViewPersistenceObject** -Datenstrom Struktur enthält Informationen zu einer Homepage-URL für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="4a5f2-126">Datenelemente in dieser Struktur werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4a5f2-127">In der folgenden Beschreibung werden möglicherweise nicht alle von Outlook unterstützten Feldwerte aufgeführt; Wenn Ihr Code also einen vorhandenen Stream liest, werden möglicherweise auch einige Flags gefunden, die hier nicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="4a5f2-128">Sie können diese Beschreibung jedoch zum programmgesteuerten Erstellen von Werten für die **PidTagFolderWebViewInfo** -Eigenschaft verwenden, die Outlook verstehen wird.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="4a5f2-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-129">_dwVersion_</span></span>
  
> <span data-ttu-id="4a5f2-130">DWORD (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-130">DWORD (4 bytes).</span></span> <span data-ttu-id="4a5f2-131">Die Version des Formats der Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-131">The version of the structure's format.</span></span> <span data-ttu-id="4a5f2-132">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="4a5f2-133">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-133">**Value name**</span></span>|<span data-ttu-id="4a5f2-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a5f2-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="4a5f2-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="4a5f2-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4a5f2-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="4a5f2-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-137">_dwType_</span></span>
  
> <span data-ttu-id="4a5f2-138">DWORD (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-138">DWORD (4 bytes).</span></span> <span data-ttu-id="4a5f2-139">Der Typ der Homepage Informationen.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-139">The type of the home page information.</span></span> <span data-ttu-id="4a5f2-140">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="4a5f2-141">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-141">**Value name**</span></span>|<span data-ttu-id="4a5f2-142">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a5f2-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="4a5f2-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="4a5f2-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a5f2-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="4a5f2-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-145">_dwFlags_</span></span>
  
> <span data-ttu-id="4a5f2-146">DWORD (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-146">DWORD (4 bytes).</span></span> <span data-ttu-id="4a5f2-147">Eine Kombination aus null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="4a5f2-148">Kennzeichenname \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4a5f2-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="4a5f2-149">\*\*\*\*Value\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4a5f2-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="4a5f2-150">\*\*\*\*Beschreibung\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4a5f2-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a5f2-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4a5f2-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="4a5f2-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a5f2-152">0x00000001</span></span>  <br/> |<span data-ttu-id="4a5f2-153">Das Kontrollkästchen **Homepage standardmäßig für diesen Ordner anzeigen** wurde auf der Registerkarte **Startseite** des Dialogfelds Eigenschaften für einen Ordner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="4a5f2-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="4a5f2-155">Ein Array von 7 DWORD-Elementen (insgesamt 28 Byte).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="4a5f2-156">Nicht verwendete.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-156">Unused.</span></span>
    
<span data-ttu-id="4a5f2-157">cbData</span><span class="sxs-lookup"><span data-stu-id="4a5f2-157">cbData</span></span>
  
> <span data-ttu-id="4a5f2-158">Ein ULONG (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="4a5f2-159">Die Größe des _wzURL_ -Datenelements in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="4a5f2-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-160">_wzURL_</span></span>
  
> <span data-ttu-id="4a5f2-161">Ein Array von Typ WCHAR-Elementen.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-161">An array of WCHAR elements.</span></span> <span data-ttu-id="4a5f2-162">Die UTF-16-Darstellung der nullterminierten URL-Zeichenfolge der Startseite.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="4a5f2-163">WebViewPersistenceObject-Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a5f2-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="4a5f2-164">In diesem Abschnitt wird ein Beispiel für einen **WebViewPersistenceObject** -Stream beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="4a5f2-165">Der Stream gibt die URLhttps://www.microsoft.comder Startseite an.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="4a5f2-166">**Daten Dump**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-166">**Data dump**</span></span>
  
<span data-ttu-id="4a5f2-167">Es folgt ein Daten Dump des Streams, wie er in einem binären Editor angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="4a5f2-168">**Datenstrom Offset**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-168">**Stream offset**</span></span>|<span data-ttu-id="4a5f2-169">**Datenbytes**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-169">**Data bytes**</span></span>|<span data-ttu-id="4a5f2-170">**ASCII-Daten**</span><span class="sxs-lookup"><span data-stu-id="4a5f2-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a5f2-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="4a5f2-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="4a5f2-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="4a5f2-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="4a5f2-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="4a5f2-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="4a5f2-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="4a5f2-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="4a5f2-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="4a5f2-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="4a5f2-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="4a5f2-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="4a5f2-177">Es folgt eine Analyse der Beispieldaten für den **WebViewPersistenceObject** -Stream.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="4a5f2-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-178">_dwVersion_</span></span>
  
> <span data-ttu-id="4a5f2-179">Offset 0x0 festlegen bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="4a5f2-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-180">_dwType_</span></span>
  
> <span data-ttu-id="4a5f2-181">Offset 0x4 bytes: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="4a5f2-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-182">_dwFlags_</span></span>
  
> <span data-ttu-id="4a5f2-183">Offset 0x8 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="4a5f2-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="4a5f2-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="4a5f2-185">Offset 0xC, 28 Byte: alle Nullen.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="4a5f2-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-186">_cbData_</span></span>
  
> <span data-ttu-id="4a5f2-187">Offset 0x28 bytes: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="4a5f2-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="4a5f2-188">_wzURL_</span></span>
  
> <span data-ttu-id="4a5f2-189">Offset 0X2c beansprucht, 0x32 bytes: Array von 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="4a5f2-190">Ein Unicode-Wert mit der Zeichenfolge 0https://www.microsoft.com(null): "".</span><span class="sxs-lookup"><span data-stu-id="4a5f2-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

