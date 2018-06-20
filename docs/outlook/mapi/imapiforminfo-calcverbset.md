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
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792163"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="8d9e0-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="8d9e0-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="8d9e0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d9e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d9e0-105">Gibt einen Zeiger auf den vollständigen Satz von Verben, die ein Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="8d9e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d9e0-106">Parameters</span></span>

 <span data-ttu-id="8d9e0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d9e0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8d9e0-108">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="8d9e0-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8d9e0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8d9e0-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d9e0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d9e0-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="8d9e0-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8d9e0-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="8d9e0-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="8d9e0-114">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIVerbArray](smapiverbarray.md) -Struktur, die dem Formular zugrunde Verben enthält.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d9e0-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8d9e0-115">Return value</span></span>

<span data-ttu-id="8d9e0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d9e0-116">S_OK</span></span> 
  
> <span data-ttu-id="8d9e0-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8d9e0-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8d9e0-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8d9e0-119">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d9e0-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d9e0-120">Remarks</span></span>

<span data-ttu-id="8d9e0-121">Clientanwendungen rufen Sie die **IMAPIFormInfo::CalcVerbSet** -Methode, um einen Zeiger auf den Satz von Verben, die von einem Formular verwendeten abrufen.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="8d9e0-122">In der **SMAPIVerbArray** -Struktur, die in der _PpMAPIVerbArray_ -Parameter zurückgegeben werden die Verben in der Reihenfolge der Indexnummer zurückgegeben. Index des Verbs wird in seinem **lVerb** Mitglied gefunden.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="8d9e0-123">Clientanwendungen können das Verb Array dynamisch erstellen Menüs, ausblenden oder Schaltflächen anzeigen, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d9e0-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="8d9e0-124">MFCMAPI reference</span></span>

<span data-ttu-id="8d9e0-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d9e0-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8d9e0-126">**File**</span></span>|<span data-ttu-id="8d9e0-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8d9e0-127">**Function**</span></span>|<span data-ttu-id="8d9e0-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8d9e0-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d9e0-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="8d9e0-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="8d9e0-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="8d9e0-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="8d9e0-131">MFCMAPI (engl.) verwendet die **IMAPIFormInfo::CalcVerbSet** -Methode beim Schreiben der Debugausgabe für Formular Informationen-Objekte.</span><span class="sxs-lookup"><span data-stu-id="8d9e0-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d9e0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d9e0-132">See also</span></span>



[<span data-ttu-id="8d9e0-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="8d9e0-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="8d9e0-134">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d9e0-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="8d9e0-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8d9e0-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
