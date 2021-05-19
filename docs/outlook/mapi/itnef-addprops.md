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
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348622"
---
# <a name="itnefaddprops"></a><span data-ttu-id="2e03b-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2e03b-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="2e03b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e03b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e03b-105">Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage.</span><span class="sxs-lookup"><span data-stu-id="2e03b-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="2e03b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e03b-106">Parameters</span></span>

 <span data-ttu-id="2e03b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e03b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2e03b-108">[in] Eine Bitmaske von Flags, die steuert, wie Eigenschaften in die Kapselung eingeschlossen oder von der Kapselung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2e03b-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="2e03b-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2e03b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2e03b-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="2e03b-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="2e03b-111">Codiert nur die Eigenschaften im  _lpPropList-Parameter,_ die Teil von Anlagen in der Nachricht sind.</span><span class="sxs-lookup"><span data-stu-id="2e03b-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="2e03b-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="2e03b-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="2e03b-113">Codiert nur Eigenschaften aus der anlage, die durch den  _ulElemID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="2e03b-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="2e03b-114">Wenn der  _lpvData-Parameter_ nicht NULL ist, werden die daten, auf die verwiesen wird, in die Kapselung der Anlage in der Datei geschrieben, die durch die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e03b-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="2e03b-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="2e03b-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="2e03b-116">Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="2e03b-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="2e03b-117">Wenn dieses Flag festgelegt ist, muss der Wert in  _lpvData_ ein [IStream-Zeiger](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) sein.</span><span class="sxs-lookup"><span data-stu-id="2e03b-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="2e03b-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="2e03b-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="2e03b-119">Codiert alle Eigenschaften, die nicht im  _lpPropList-Parameter angegeben_ sind.</span><span class="sxs-lookup"><span data-stu-id="2e03b-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="2e03b-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="2e03b-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="2e03b-121">Codiert alle in  _lpPropList_ angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e03b-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="2e03b-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="2e03b-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="2e03b-123">Codiert nur die in  _lpPropList_ angegebenen Eigenschaften, die Teil der Nachricht selbst sind.</span><span class="sxs-lookup"><span data-stu-id="2e03b-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="2e03b-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="2e03b-124">_ulElemID_</span></span>
  
> <span data-ttu-id="2e03b-125">[in] Die eigenschaft PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in ihrer übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2e03b-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="2e03b-126">Der  _ulElemID-Parameter_ wird verwendet, wenn eine spezielle Behandlung für eine Anlage angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="2e03b-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="2e03b-127">Der  _ulElemID-Parameter_ sollte 0 sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF im  _ulFlags-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="2e03b-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2e03b-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="2e03b-128">_lpvData_</span></span>
  
> <span data-ttu-id="2e03b-129">[in] Ein Zeiger auf Anlagendaten, die zum Ersetzen der In _ulElemID angegebenen Anlagendaten verwendet werden._</span><span class="sxs-lookup"><span data-stu-id="2e03b-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="2e03b-130">Der _lpvData-Parameter_ sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="2e03b-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2e03b-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="2e03b-131">_lpPropList_</span></span>
  
> <span data-ttu-id="2e03b-132">[in] Ein Zeiger auf die Liste der Eigenschaften, die in die Kapselung aufgenommen oder von der Kapselung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2e03b-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e03b-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e03b-133">Return value</span></span>

<span data-ttu-id="2e03b-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e03b-134">S_OK</span></span> 
  
> <span data-ttu-id="2e03b-135">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2e03b-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e03b-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e03b-136">Remarks</span></span>

<span data-ttu-id="2e03b-137">Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::AddProps-Methode** auf, um Eigenschaften auflisten, die in die Transport-Neutral Encapsulation Format (TNEF)-Verarbeitung einer Nachricht oder Anlage eingeschlossen oder von dieser ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e03b-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="2e03b-138">Durch die Verwendung aufeinander folgenden Aufrufs kann der Anbieter oder das Gateway eine Liste der Eigenschaften angeben, die hinzugefügt und codiert oder von der Codierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2e03b-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="2e03b-139">Anbieter und Gateways können auch **AddProps** verwenden, um Informationen zu speziellen Behandlungsanlagen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="2e03b-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="2e03b-140">**AddProps wird** nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion geöffnet](opentnefstreamex.md) werden.</span><span class="sxs-lookup"><span data-stu-id="2e03b-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="2e03b-141">Beachten Sie, dass keine tatsächliche TNEF-Codierung für **AddProps** erfolgt, bis die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e03b-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="2e03b-142">Diese Funktionalität bedeutet, dass Zeiger, die an **AddProps übergeben** werden, gültig bleiben müssen, bis der Aufruf von **Finish** erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="2e03b-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="2e03b-143">An diesem Punkt können alle Objekte und Daten, die mit **AddProps-Aufrufen** übergeben werden, freigegeben oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e03b-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2e03b-144">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="2e03b-144">MFCMAPI reference</span></span>

<span data-ttu-id="2e03b-145">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2e03b-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2e03b-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2e03b-146">**File**</span></span>|<span data-ttu-id="2e03b-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2e03b-147">**Function**</span></span>|<span data-ttu-id="2e03b-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2e03b-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e03b-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="2e03b-149">File.cpp</span></span>  <br/> |<span data-ttu-id="2e03b-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="2e03b-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="2e03b-151">MFCMAPI verwendet die **ITnef::AddProps-Methode,** um Eigenschaften aus einer Nachricht in einen TNEF-Stream zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2e03b-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e03b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e03b-152">See also</span></span>



[<span data-ttu-id="2e03b-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="2e03b-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="2e03b-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="2e03b-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="2e03b-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="2e03b-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="2e03b-156">PidTagAttachTransportName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2e03b-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="2e03b-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e03b-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="2e03b-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2e03b-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

