---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792165"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="7ca82-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="7ca82-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="7ca82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ca82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ca82-105">Erstellt ein Symbol aus der Symboleigenschaften eines Formulars an.</span><span class="sxs-lookup"><span data-stu-id="7ca82-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="7ca82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ca82-106">Parameters</span></span>

 <span data-ttu-id="7ca82-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="7ca82-107">_nPropID_</span></span>
  
> <span data-ttu-id="7ca82-108">[in] Ein Bezeichner für ein Icon-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ca82-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="7ca82-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="7ca82-109">_phicon_</span></span>
  
> <span data-ttu-id="7ca82-110">[out] Ein Zeiger auf das zurückgegebene Symbol.</span><span class="sxs-lookup"><span data-stu-id="7ca82-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ca82-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ca82-111">Return value</span></span>

<span data-ttu-id="7ca82-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ca82-112">S_OK</span></span> 
  
> <span data-ttu-id="7ca82-113">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7ca82-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ca82-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ca82-114">Remarks</span></span>

<span data-ttu-id="7ca82-115">Clientanwendungen rufen Sie die **IMAPIFormInfo::MakeIconFromBinary** -Methode, um ein Symbol aus der Symboleigenschaften eines Formulars zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ca82-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="7ca82-116">In den _nPropID_ -Parameter akzeptiert **MakeIconFromBinary** der Bezeichner der der Symboleigenschaften eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="7ca82-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="7ca82-117">Mit dieser Eigenschaftenbezeichner, erstellt er ein Symbol, das in der Tabelle angezeigt werden kann, die Eigenschaftenspalten für Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ca82-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ca82-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ca82-118">See also</span></span>



[<span data-ttu-id="7ca82-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ca82-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

