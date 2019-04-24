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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348622"
---
# <a name="itnefaddprops"></a><span data-ttu-id="bd910-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="bd910-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="bd910-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd910-105">Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage.</span><span class="sxs-lookup"><span data-stu-id="bd910-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="bd910-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd910-106">Parameters</span></span>

 <span data-ttu-id="bd910-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd910-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bd910-108">in Eine Bitmaske von Flags, die steuert, wie Eigenschaften in Kapselung eingeschlossen oder von dieser ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="bd910-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="bd910-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bd910-109">The following flags can be set:</span></span>
    
<span data-ttu-id="bd910-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="bd910-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="bd910-111">Codiert nur die Eigenschaften im _lpPropList_ -Parameter, die Teil von Anlagen in der Nachricht sind.</span><span class="sxs-lookup"><span data-stu-id="bd910-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="bd910-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="bd910-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="bd910-113">Codiert nur Eigenschaften aus der Anlage, die durch den _ulElemID_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd910-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="bd910-114">Wenn der _lpvData_ -Parameter nicht NULL ist, werden die Daten, auf die verwiesen wird, in die Kapselung der Anlage in der durch die **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft angegebenen Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd910-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="bd910-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="bd910-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="bd910-116">Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den _ulElemID_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd910-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="bd910-117">Wenn dieses Flag festgelegt ist, muss der Wert in _lpvData_ ein [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="bd910-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="bd910-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="bd910-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="bd910-119">Codiert alle Eigenschaften, die nicht im _lpPropList_ -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bd910-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="bd910-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="bd910-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="bd910-121">Codiert alle in _lpPropList_angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bd910-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="bd910-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="bd910-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="bd910-123">Codiert nur die in _lpPropList_ angegebenen Eigenschaften, die Teil der Nachricht selbst sind.</span><span class="sxs-lookup"><span data-stu-id="bd910-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="bd910-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="bd910-124">_ulElemID_</span></span>
  
> <span data-ttu-id="bd910-125">in Die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bd910-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="bd910-126">Der Parameter _ulElemID_ wird verwendet, wenn eine spezielle Behandlung für eine Anlage angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="bd910-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="bd910-127">Der _ulElemID_ -Parameter sollte 0 sein, es sei denn, das TNEF_PROP_CONTAINED-oder TNEF_PROP_CONTAINED_TNEF-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd910-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bd910-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="bd910-128">_lpvData_</span></span>
  
> <span data-ttu-id="bd910-129">in Ein Zeiger auf Anlagendaten, die zum Ersetzen der Daten der in _ulElemID_angegebenen Anlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd910-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="bd910-130">Der _lpvData_ -Parameter sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF ist in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd910-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="bd910-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="bd910-131">_lpPropList_</span></span>
  
> <span data-ttu-id="bd910-132">in Ein Zeiger auf die Liste der Eigenschaften, die in Kapselung eingeschlossen oder von dieser ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd910-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd910-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd910-133">Return value</span></span>

<span data-ttu-id="bd910-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd910-134">S_OK</span></span> 
  
> <span data-ttu-id="bd910-135">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bd910-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd910-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd910-136">Remarks</span></span>

<span data-ttu-id="bd910-137">Transportanbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef::** AddProps-Methode auf, um Eigenschaften aufzulisten, die in die TNEF-Verarbeitung (Transport Neutral Encapsulation Format) einer Nachricht oder Anlage eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd910-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="bd910-138">Durch die Verwendung aufeinanderfolgender Aufrufe kann der Anbieter oder das Gateway eine Liste von Eigenschaften angeben, die hinzugefügt und codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd910-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="bd910-139">Anbieter und Gateways können auch addProps verwenden, um Informationen über sonderbehandlungs Anlagen bereitzustellen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bd910-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="bd910-140">\*\*\*\* AddProps wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="bd910-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="bd910-141">Beachten Sie, dass keine tatsächliche TNEF- \*\*\*\* Codierung für AddProps erfolgt, bis die [ITnef:: Finish](itnef-finish.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bd910-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="bd910-142">Diese Funktionalität bedeutet, dass Zeiger, \*\*\*\* die an AddProps übergeben werden, gültig bleiben müssen, bis der Aufruf **beendet** wurde.</span><span class="sxs-lookup"><span data-stu-id="bd910-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="bd910-143">An diesem Punkt können alle Objekte und Daten, die mit \*\*\*\* AddProps-aufrufen übergeben wurden, freigegeben oder befreit werden.</span><span class="sxs-lookup"><span data-stu-id="bd910-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bd910-144">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="bd910-144">MFCMAPI reference</span></span>

<span data-ttu-id="bd910-145">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bd910-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bd910-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="bd910-146">**File**</span></span>|<span data-ttu-id="bd910-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bd910-147">**Function**</span></span>|<span data-ttu-id="bd910-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="bd910-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd910-149">Datei. cpp</span><span class="sxs-lookup"><span data-stu-id="bd910-149">File.cpp</span></span>  <br/> |<span data-ttu-id="bd910-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="bd910-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="bd910-151">MFCMAPI verwendet die **ITnef::** AddProps-Methode, um Eigenschaften aus einer Nachricht in einen TNEF-Stream zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="bd910-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd910-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd910-152">See also</span></span>



[<span data-ttu-id="bd910-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="bd910-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="bd910-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="bd910-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="bd910-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="bd910-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="bd910-156">Kanonische Pidtagattachtransportname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bd910-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="bd910-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd910-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="bd910-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="bd910-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

