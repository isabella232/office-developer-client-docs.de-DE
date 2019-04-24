---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321694"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="8186e-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="8186e-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="8186e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8186e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8186e-105">Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, die ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="8186e-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="8186e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8186e-106">Parameters</span></span>

 <span data-ttu-id="8186e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8186e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8186e-108">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="8186e-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="8186e-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8186e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8186e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8186e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8186e-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8186e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="8186e-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8186e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8186e-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="8186e-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="8186e-114">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIVerbArray](smapiverbarray.md) -Struktur, die die Verben des Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="8186e-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8186e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8186e-115">Return value</span></span>

<span data-ttu-id="8186e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8186e-116">S_OK</span></span> 
  
> <span data-ttu-id="8186e-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8186e-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8186e-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8186e-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8186e-119">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="8186e-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8186e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8186e-120">Remarks</span></span>

<span data-ttu-id="8186e-121">Client Anwendungen rufen die **IMAPIFormInfo:: CalcVerbSet** -Methode auf, um einen Zeiger auf die von einem Formular verwendete Verben abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8186e-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="8186e-122">In der **SMAPIVerbArray** -Struktur, die im Parameter _ppMAPIVerbArray_ zurückgegeben wird, werden die Verben in der Reihenfolge der Indexnummer zurückgegeben. jeder Verb Index wird im **lVerb** -Element gefunden.</span><span class="sxs-lookup"><span data-stu-id="8186e-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="8186e-123">Client Anwendungen können das Verb-Array verwenden, um Menüs dynamisch zu erstellen, Schaltflächen ein-oder auszublenden usw.</span><span class="sxs-lookup"><span data-stu-id="8186e-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8186e-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8186e-124">MFCMAPI reference</span></span>

<span data-ttu-id="8186e-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8186e-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8186e-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8186e-126">**File**</span></span>|<span data-ttu-id="8186e-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8186e-127">**Function**</span></span>|<span data-ttu-id="8186e-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8186e-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8186e-129">MFCOutput. cpp</span><span class="sxs-lookup"><span data-stu-id="8186e-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="8186e-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="8186e-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="8186e-131">MFCMAPI verwendet die **IMAPIFormInfo:: CalcVerbSet** -Methode beim Schreiben der Debug-Ausgabe für Formular Informationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="8186e-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8186e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8186e-132">See also</span></span>



[<span data-ttu-id="8186e-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="8186e-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="8186e-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8186e-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="8186e-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8186e-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

