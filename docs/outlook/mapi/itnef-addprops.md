---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792849"
---
# <a name="itnefaddprops"></a><span data-ttu-id="1588a-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="1588a-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="1588a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1588a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1588a-105">Ermöglicht die aufrufende Dienstanbieter oder Gateway Eigenschaften, die Kapselung einer Nachricht oder eine Anlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1588a-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="1588a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1588a-106">Parameters</span></span>

 <span data-ttu-id="1588a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1588a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1588a-108">[in] Eine Bitmaske aus Flags, die steuert, wie Eigenschaften eingeschlossen oder ausgeschlossen Kapselung.</span><span class="sxs-lookup"><span data-stu-id="1588a-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="1588a-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1588a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="1588a-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="1588a-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="1588a-111">Nur die Eigenschaften im _LpPropList_ -Parameter, die Teil von Anlagen in der Nachricht sind codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="1588a-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="1588a-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="1588a-113">Nur Eigenschaften aus der Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="1588a-114">Wenn der Parameter _LpvData_ nicht NULL ist, werden die Daten, auf in die Anlage-Kapselung in der durch die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))-Eigenschaft angegebenen Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1588a-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="1588a-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="1588a-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="1588a-116">Nur Eigenschaften aus der Nachricht oder einer Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="1588a-117">Wenn dieses Flag festgelegt ist, muss der Wert in _LpvData_ ein [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="1588a-117">If this flag is set, the value in  _lpvData_ must be an [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) pointer.</span></span> 
    
<span data-ttu-id="1588a-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="1588a-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="1588a-119">Codiert alle Eigenschaften in der _LpPropList_ -Parameter nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="1588a-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="1588a-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="1588a-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="1588a-121">Alle Eigenschaften in _LpPropList_codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="1588a-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="1588a-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="1588a-123">Nur die Eigenschaften im _LpPropList_ angegeben, die Teil einer Nachricht sind codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="1588a-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="1588a-124">_ulElemID_</span></span>
  
> <span data-ttu-id="1588a-125">[in] Eine Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft, die eine Zahl, eindeutig enthält identifiziert die Anlage in der übergeordneten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1588a-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="1588a-126">Der Parameter _UlElemID_ wird verwendet, wenn besondere Behandlung für eine Anlage angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="1588a-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="1588a-127">Der Parameter _UlElemID_ muss 0 sein, es sei denn, das Flag TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1588a-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1588a-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="1588a-128">_lpvData_</span></span>
  
> <span data-ttu-id="1588a-129">[in] Ein Zeiger auf Anlagedaten verwendet, um die Daten der Anlage in _UlElemID_angegebenen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1588a-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="1588a-130">Der Parameter _LpvData_ sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1588a-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1588a-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="1588a-131">_lpPropList_</span></span>
  
> <span data-ttu-id="1588a-132">[in] Ein Zeiger auf die Liste der Eigenschaften ein-oder Ausschließen von Kapselung.</span><span class="sxs-lookup"><span data-stu-id="1588a-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1588a-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1588a-133">Return value</span></span>

<span data-ttu-id="1588a-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="1588a-134">S_OK</span></span> 
  
> <span data-ttu-id="1588a-135">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1588a-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1588a-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1588a-136">Remarks</span></span>

<span data-ttu-id="1588a-137">Transport-Provider, Anbieter Nachricht und Gateways rufen Sie die **ITnef::AddProps** -Methode, die Listeneigenschaften aufgenommen oder aus der Verarbeitung Transport-Neutral Encapsulation Format (TNEF) einer Nachricht oder eine Anlage ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1588a-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="1588a-138">Mithilfe von aufeinander folgenden aufrufen, kann die Anbieter oder das Gateway angeben eine Liste der Eigenschaften, die Sie hinzufügen und codieren oder ausgeschlossen werden codiert.</span><span class="sxs-lookup"><span data-stu-id="1588a-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="1588a-139">Anbieter und Gateways können **AddProps** auch zum Bereitstellen von Informationen über alle Anlagen besondere Behandlung gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1588a-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="1588a-140">**AddProps** wird nur für TNEF-Objekten unterstützt, die mit dem TNEF_ENCODE-Flag für die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="1588a-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="1588a-141">Beachten Sie, dass keine tatsächliche TNEF-Codierung geschieht für **AddProps** , bis die [ITnef::Finish](itnef-finish.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1588a-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="1588a-142">Dies bedeutet, dass Zeiger in **AddProps** übergeben gültig bis bleiben müssen nach dem Anruf auf **Fertig stellen** .</span><span class="sxs-lookup"><span data-stu-id="1588a-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="1588a-143">An dieser Stelle können alle Objekte und Daten mit **AddProps** Anrufe übergebene freigegeben oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1588a-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1588a-144">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="1588a-144">MFCMAPI reference</span></span>

<span data-ttu-id="1588a-145">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1588a-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1588a-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1588a-146">**File**</span></span>|<span data-ttu-id="1588a-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1588a-147">**Function**</span></span>|<span data-ttu-id="1588a-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1588a-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1588a-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1588a-149">File.cpp</span></span>  <br/> |<span data-ttu-id="1588a-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="1588a-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="1588a-151">MFCMAPI (engl.) verwendet die **ITnef::AddProps** -Methode, um Eigenschaften aus einer Nachricht in einem Stream TNEF zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1588a-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1588a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1588a-152">See also</span></span>



[<span data-ttu-id="1588a-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="1588a-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="1588a-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="1588a-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="1588a-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="1588a-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="1588a-156">PidTagAttachTransportName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1588a-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="1588a-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1588a-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="1588a-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1588a-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

