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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 62bc0e75d0a405ebe9f68ec9f4af1ca038bda219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794400"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="70236-103">PidTagFolderWebViewInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70236-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="70236-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70236-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70236-105">Enthält die URL für die Homepage eines Ordners in Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="70236-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="70236-106">Diese Eigenschaft enthält einen binären Datenstrom **WebViewPersistenceObject**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="70236-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70236-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="70236-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="70236-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="70236-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="70236-109">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="70236-109">Identifier:</span></span>  <br/> |<span data-ttu-id="70236-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="70236-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="70236-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="70236-111">Data type:</span></span>  <br/> |<span data-ttu-id="70236-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70236-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70236-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="70236-113">Area:</span></span>  <br/> |<span data-ttu-id="70236-114">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="70236-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70236-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70236-115">Remarks</span></span>

<span data-ttu-id="70236-116">URL der Startseite kann für alle Outlook-Ordner angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70236-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="70236-117">Diese Informationen kann über die Registerkarte " **Homepage** " im Dialogfeld Eigenschaften für einen Ordner in Outlook zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="70236-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="70236-118">Je nach bestimmten Richtlinieneinstellungen möglicherweise auf der Startseite von Outlook ignoriert, wenn der MAPI-Informationsspeicher, der dieser Ordner enthält keine MSCAP_SECURE_FOLDER_HOMEPAGES in seiner Implementierung [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) meldet.</span><span class="sxs-lookup"><span data-stu-id="70236-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="70236-119">Den Ordner **Outlook Heute** und einem öffentlichen Ordner können Homepage-URLs haben.</span><span class="sxs-lookup"><span data-stu-id="70236-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="70236-120">Der Ordner **Outlook Heute** verwendet jedoch einen anderen Mechanismus zum Verwalten von des URL der Startseite; Dieser Mechanismus ist nicht in diesem Thema behandelt.</span><span class="sxs-lookup"><span data-stu-id="70236-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="70236-121">Ein öffentlicher Ordner möglicherweise auch eine Homepage-URL definiert, die für einen Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="70236-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="70236-122">Diese Funktion wird jedoch nicht in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="70236-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="70236-123">Der Wert dieser Eigenschaft ist einen binären Datenstrom **WebViewPersistenceObject**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="70236-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="70236-124">WebViewPersistenceObject Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="70236-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="70236-125">Die **WebViewPersistenceObject** Stream-Datenstruktur enthält Informationen über eine Homepage-URL für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="70236-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="70236-126">Data-Elemente in dieser Struktur werden in little-Endian-Bytereihenfolge, unmittelbar auf voneinander in der angegebenen Reihenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70236-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="70236-127">In der folgenden Beschreibung möglicherweise nicht Auflisten aller die Feldwerte von Outlook unterstützt; aus diesem Grund, wenn der Code einen vorhandenen Stream liest, möglicherweise einige Flags, die hier nicht aufgeführt sind auch gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="70236-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="70236-128">Diese Beschreibung können Sie jedoch die um Werte für die **PidTagFolderWebViewInfo** -Eigenschaft programmgesteuert zu erstellen, die Outlook verstehen.</span><span class="sxs-lookup"><span data-stu-id="70236-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="70236-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="70236-129">_dwVersion_</span></span>
  
> <span data-ttu-id="70236-130">Ein DWORD-Wert (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="70236-130">DWORD (4 bytes).</span></span> <span data-ttu-id="70236-131">Die Version des Formats der Struktur.</span><span class="sxs-lookup"><span data-stu-id="70236-131">The version of the structure's format.</span></span> <span data-ttu-id="70236-132">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="70236-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="70236-133">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="70236-133">**Value name**</span></span>|<span data-ttu-id="70236-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="70236-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70236-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="70236-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="70236-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70236-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="70236-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="70236-137">_dwType_</span></span>
  
> <span data-ttu-id="70236-138">Ein DWORD-Wert (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="70236-138">DWORD (4 bytes).</span></span> <span data-ttu-id="70236-139">Der Typ der Informationen zur Homepage.</span><span class="sxs-lookup"><span data-stu-id="70236-139">The type of the home page information.</span></span> <span data-ttu-id="70236-140">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="70236-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="70236-141">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="70236-141">**Value name**</span></span>|<span data-ttu-id="70236-142">**Wert**</span><span class="sxs-lookup"><span data-stu-id="70236-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70236-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="70236-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="70236-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70236-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="70236-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="70236-145">_dwFlags_</span></span>
  
> <span data-ttu-id="70236-146">Ein DWORD-Wert (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="70236-146">DWORD (4 bytes).</span></span> <span data-ttu-id="70236-147">Eine Kombination aus null oder mehr flags, deren Werte und Bedeutung sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="70236-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="70236-148">Flag Namen \*\*\*</span><span class="sxs-lookup"><span data-stu-id="70236-148">****Flag name****</span></span>|<span data-ttu-id="70236-149">Wert \*\*\*</span><span class="sxs-lookup"><span data-stu-id="70236-149">****Value****</span></span>|<span data-ttu-id="70236-150">****Beschreibung****</span><span class="sxs-lookup"><span data-stu-id="70236-150">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="70236-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="70236-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="70236-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70236-152">0x00000001</span></span>  <br/> |<span data-ttu-id="70236-153">Aktivieren Sie das Kontrollkästchen **Homepage in der Standardeinstellung für diesen Ordner anzeigen** wurde in der Registerkarte **Startseite** im Dialogfeld Eigenschaften für einen Ordner überprüft.</span><span class="sxs-lookup"><span data-stu-id="70236-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="70236-154">_DwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="70236-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="70236-155">Ein Array von 7 DWORD-Elemente (insgesamt 28 Bytes).</span><span class="sxs-lookup"><span data-stu-id="70236-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="70236-156">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="70236-156">Unused.</span></span>
    
<span data-ttu-id="70236-157">cbData</span><span class="sxs-lookup"><span data-stu-id="70236-157">cbData</span></span>
  
> <span data-ttu-id="70236-158">Ein ULONG (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="70236-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="70236-159">Die Größe des _WzURL_ -Data-Element in Bytes.</span><span class="sxs-lookup"><span data-stu-id="70236-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="70236-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="70236-160">_wzURL_</span></span>
  
> <span data-ttu-id="70236-161">Ein Array von WCHAR Elemente.</span><span class="sxs-lookup"><span data-stu-id="70236-161">An array of WCHAR elements.</span></span> <span data-ttu-id="70236-162">Die UTF-16-Darstellung der URL Homepage NULL endende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70236-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="70236-163">WebViewPersistenceObject Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="70236-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="70236-164">Dieser Abschnitt beschreibt ein Beispiel eines **WebViewPersistenceObject** Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="70236-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="70236-165">Das Stream-Objekt gibt die URL der Startseite "http://www.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="70236-165">The stream specifies the home page URL "http://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="70236-166">**Daten dump**</span><span class="sxs-lookup"><span data-stu-id="70236-166">**Data dump**</span></span>
  
<span data-ttu-id="70236-167">Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70236-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="70236-168">**Stream-offset**</span><span class="sxs-lookup"><span data-stu-id="70236-168">**Stream offset**</span></span>|<span data-ttu-id="70236-169">**Datenbytes**</span><span class="sxs-lookup"><span data-stu-id="70236-169">**Data bytes**</span></span>|<span data-ttu-id="70236-170">**ASCII-Daten**</span><span class="sxs-lookup"><span data-stu-id="70236-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="70236-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="70236-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="70236-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="70236-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="70236-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="70236-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="70236-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="70236-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="70236-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="70236-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="70236-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="70236-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="70236-177">Es folgt eine Analyse der Beispieldaten für den **WebViewPersistenceObject** -Stream.</span><span class="sxs-lookup"><span data-stu-id="70236-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="70236-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="70236-178">_dwVersion_</span></span>
  
> <span data-ttu-id="70236-179">Offset 0 x 0, 4 Bytes: 0 x 00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="70236-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="70236-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="70236-180">_dwType_</span></span>
  
> <span data-ttu-id="70236-181">Offset 0, 4 Bytes x 4: 0 x 00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="70236-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="70236-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="70236-182">_dwFlags_</span></span>
  
> <span data-ttu-id="70236-183">Offset 0 x 8, 4 Bytes: 0 x 00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="70236-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="70236-184">_DwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="70236-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="70236-185">Offset 0xC 28 Bytes: Nullen.</span><span class="sxs-lookup"><span data-stu-id="70236-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="70236-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="70236-186">_cbData_</span></span>
  
> <span data-ttu-id="70236-187">Offset 0, 4 Bytes x 28: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="70236-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="70236-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="70236-188">_wzURL_</span></span>
  
> <span data-ttu-id="70236-189">Offset 0x2C, 0 x 32 Bytes: Array von 25 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="70236-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="70236-190">Unicode-Wert NULL endende Zeichenfolge: "http://www.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="70236-190">A Unicode zero-terminated string value: "http://www.microsoft.com".</span></span>
    

