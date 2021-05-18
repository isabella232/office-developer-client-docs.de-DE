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
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316310"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="03ea3-103">PidTagFolderWebViewInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03ea3-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="03ea3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03ea3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03ea3-105">Enthält die URL für die Homepage eines Ordners in Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="03ea3-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="03ea3-106">Diese Eigenschaft enthält einen binären Datenstrom namens **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="03ea3-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03ea3-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03ea3-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="03ea3-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="03ea3-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="03ea3-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="03ea3-109">Identifier:</span></span>  <br/> |<span data-ttu-id="03ea3-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="03ea3-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="03ea3-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03ea3-111">Data type:</span></span>  <br/> |<span data-ttu-id="03ea3-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03ea3-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03ea3-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03ea3-113">Area:</span></span>  <br/> |<span data-ttu-id="03ea3-114">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="03ea3-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03ea3-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03ea3-115">Remarks</span></span>

<span data-ttu-id="03ea3-116">Eine Homepage-URL kann für jeden beliebigen Ordner Outlook werden.</span><span class="sxs-lookup"><span data-stu-id="03ea3-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="03ea3-117">Auf diese Informationen kann in Outlook  der Registerkarte Startseite des Dialogfelds Eigenschaften für einen Ordner zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="03ea3-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="03ea3-118">Abhängig von bestimmten Richtlinieneinstellungen wird die Startseite möglicherweise von Outlook ignoriert, wenn der MAPI-Speicher, der diesen Ordner enthält, MSCAP_SECURE_FOLDER_HOMEPAGES in seiner [IMSCapabilities::GetCapabilities-Implementierung](pidtagfolderwebviewinfo-cannonical-property.md) nicht MSCAP_SECURE_FOLDER_HOMEPAGES berichtet.</span><span class="sxs-lookup"><span data-stu-id="03ea3-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="03ea3-119">Sowohl der **Outlook als** auch ein öffentlicher Ordner können URLs für die Startseite enthalten.</span><span class="sxs-lookup"><span data-stu-id="03ea3-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="03ea3-120">Der Ordner **Outlook Heute** verwendet jedoch einen anderen Mechanismus zum Verwalten der Startseiten-URL. dieser Mechanismus wird in diesem Thema nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="03ea3-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="03ea3-121">In einem öffentlichen Ordner ist möglicherweise auch eine Homepage-URL definiert, die für einen Benutzer spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="03ea3-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="03ea3-122">Diese Funktion wird in diesem Thema jedoch nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="03ea3-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="03ea3-123">Der Wert dieser Eigenschaft ist ein binärer Datenstrom namens **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="03ea3-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="03ea3-124">WebViewPersistenceObject Stream Structure</span><span class="sxs-lookup"><span data-stu-id="03ea3-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="03ea3-125">Die **WebViewPersistenceObject-Streamstruktur** enthält Informationen zu einer Homepage-URL für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="03ea3-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="03ea3-126">Datenelemente in dieser Struktur werden in der Bytereihenfolge little-endian gespeichert und folgen in der folgenden angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="03ea3-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03ea3-127">In der folgenden Beschreibung werden möglicherweise nicht alle von der Datei unterstützten Feldwerte Outlook. Wenn Ihr Code daher einen vorhandenen Datenstrom liest, werden möglicherweise auch einige Flags gefunden, die hier nicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="03ea3-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="03ea3-128">Sie können diese Beschreibung jedoch verwenden, um programmgesteuert Werte für die **PidTagFolderWebViewInfo-Eigenschaft** zu erstellen, die Outlook versteht.</span><span class="sxs-lookup"><span data-stu-id="03ea3-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="03ea3-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="03ea3-129">_dwVersion_</span></span>
  
> <span data-ttu-id="03ea3-130">DWORD (4 Byte).</span><span class="sxs-lookup"><span data-stu-id="03ea3-130">DWORD (4 bytes).</span></span> <span data-ttu-id="03ea3-131">Die Version des Strukturformats.</span><span class="sxs-lookup"><span data-stu-id="03ea3-131">The version of the structure's format.</span></span> <span data-ttu-id="03ea3-132">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="03ea3-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="03ea3-133">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="03ea3-133">**Value name**</span></span>|<span data-ttu-id="03ea3-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="03ea3-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03ea3-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="03ea3-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="03ea3-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="03ea3-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="03ea3-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="03ea3-137">_dwType_</span></span>
  
> <span data-ttu-id="03ea3-138">DWORD (4 Byte).</span><span class="sxs-lookup"><span data-stu-id="03ea3-138">DWORD (4 bytes).</span></span> <span data-ttu-id="03ea3-139">Der Typ der Startseiteninformationen.</span><span class="sxs-lookup"><span data-stu-id="03ea3-139">The type of the home page information.</span></span> <span data-ttu-id="03ea3-140">Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.</span><span class="sxs-lookup"><span data-stu-id="03ea3-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="03ea3-141">**Wertname**</span><span class="sxs-lookup"><span data-stu-id="03ea3-141">**Value name**</span></span>|<span data-ttu-id="03ea3-142">**Wert**</span><span class="sxs-lookup"><span data-stu-id="03ea3-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03ea3-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="03ea3-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="03ea3-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="03ea3-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="03ea3-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="03ea3-145">_dwFlags_</span></span>
  
> <span data-ttu-id="03ea3-146">DWORD (4 Byte).</span><span class="sxs-lookup"><span data-stu-id="03ea3-146">DWORD (4 bytes).</span></span> <span data-ttu-id="03ea3-147">Eine Kombination aus Null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="03ea3-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="03ea3-148">Kennzeichenname\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03ea3-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="03ea3-149">\*\*\*\*Value\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03ea3-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="03ea3-150">\*\*\*\*Beschreibung\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03ea3-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03ea3-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="03ea3-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="03ea3-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="03ea3-152">0x00000001</span></span>  <br/> |<span data-ttu-id="03ea3-153">Das **Kontrollkästchen Homepage für** diesen Ordner standardmäßig  anzeigen wurde auf der Registerkarte Startseite des Dialogfelds Eigenschaften für einen Ordner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="03ea3-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="03ea3-154">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="03ea3-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="03ea3-155">Ein Array von 7 DWORD-Elementen (insgesamt 28 Byte).</span><span class="sxs-lookup"><span data-stu-id="03ea3-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="03ea3-156">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ea3-156">Unused.</span></span>
    
<span data-ttu-id="03ea3-157">cbData</span><span class="sxs-lookup"><span data-stu-id="03ea3-157">cbData</span></span>
  
> <span data-ttu-id="03ea3-158">Ein ULONG (4 Byte).</span><span class="sxs-lookup"><span data-stu-id="03ea3-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="03ea3-159">Die Größe des  _wzURL-Datenelements_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="03ea3-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="03ea3-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="03ea3-160">_wzURL_</span></span>
  
> <span data-ttu-id="03ea3-161">Ein Array von WCHAR-Elementen.</span><span class="sxs-lookup"><span data-stu-id="03ea3-161">An array of WCHAR elements.</span></span> <span data-ttu-id="03ea3-162">Die UTF-16-Darstellung der URL-Zeichenfolge mit 0-gekündigter Startseite.</span><span class="sxs-lookup"><span data-stu-id="03ea3-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="03ea3-163">WebViewPersistenceObject-Streambeispiel</span><span class="sxs-lookup"><span data-stu-id="03ea3-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="03ea3-164">In diesem Abschnitt wird ein Beispiel für einen **WebViewPersistenceObject-Stream** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="03ea3-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="03ea3-165">Der Datenstrom gibt die Homepage-URL " " https://www.microsoft.com an.</span><span class="sxs-lookup"><span data-stu-id="03ea3-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="03ea3-166">**Datenabbild**</span><span class="sxs-lookup"><span data-stu-id="03ea3-166">**Data dump**</span></span>
  
<span data-ttu-id="03ea3-167">Es folgt ein Datenabbild des Datenstroms, wie er in einem binären Editor angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="03ea3-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="03ea3-168">**Stream offset**</span><span class="sxs-lookup"><span data-stu-id="03ea3-168">**Stream offset**</span></span>|<span data-ttu-id="03ea3-169">**Datenbytes**</span><span class="sxs-lookup"><span data-stu-id="03ea3-169">**Data bytes**</span></span>|<span data-ttu-id="03ea3-170">**ASCII-Daten**</span><span class="sxs-lookup"><span data-stu-id="03ea3-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03ea3-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="03ea3-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="03ea3-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="03ea3-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="03ea3-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="03ea3-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="03ea3-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="03ea3-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="03ea3-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="03ea3-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="03ea3-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="03ea3-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="03ea3-177">Im Folgenden finden Sie eine Analyse der Beispieldaten für den **WebViewPersistenceObject-Stream.**</span><span class="sxs-lookup"><span data-stu-id="03ea3-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="03ea3-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="03ea3-178">_dwVersion_</span></span>
  
> <span data-ttu-id="03ea3-179">Offset 0x0, 4 Byte: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="03ea3-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="03ea3-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="03ea3-180">_dwType_</span></span>
  
> <span data-ttu-id="03ea3-181">Offset 0x4, 4 Bytes: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="03ea3-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="03ea3-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="03ea3-182">_dwFlags_</span></span>
  
> <span data-ttu-id="03ea3-183">Offset 0x8, 4 Byte: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="03ea3-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="03ea3-184">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="03ea3-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="03ea3-185">Offset 0xC, 28 Byte: alle Nullen.</span><span class="sxs-lookup"><span data-stu-id="03ea3-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="03ea3-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="03ea3-186">_cbData_</span></span>
  
> <span data-ttu-id="03ea3-187">Offset 0x28, 4 Byte: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="03ea3-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="03ea3-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="03ea3-188">_wzURL_</span></span>
  
> <span data-ttu-id="03ea3-189">Offset 0x2C, 0x32 Bytes: Array von 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="03ea3-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="03ea3-190">Ein Unicode-Wert mit Nullendzeichenfolge: " https://www.microsoft.com ".</span><span class="sxs-lookup"><span data-stu-id="03ea3-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

