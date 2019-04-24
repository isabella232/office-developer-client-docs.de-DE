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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342112"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="76368-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="76368-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="76368-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76368-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76368-105">Erstellt ein Symbol aus einer der Symbol Eigenschaften eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="76368-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="76368-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76368-106">Parameters</span></span>

 <span data-ttu-id="76368-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="76368-107">_nPropID_</span></span>
  
> <span data-ttu-id="76368-108">in Ein Eigenschaftenbezeichner für eine Icon-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="76368-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="76368-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="76368-109">_phicon_</span></span>
  
> <span data-ttu-id="76368-110">Out Ein Zeiger auf das zurückgegebene Symbol.</span><span class="sxs-lookup"><span data-stu-id="76368-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76368-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76368-111">Return value</span></span>

<span data-ttu-id="76368-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="76368-112">S_OK</span></span> 
  
> <span data-ttu-id="76368-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="76368-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76368-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76368-114">Remarks</span></span>

<span data-ttu-id="76368-115">Client Anwendungen rufen die **IMAPIFormInfo:: MakeIconFromBinary** -Methode auf, um ein Symbol aus einer der Symbol Eigenschaften eines Formulars zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76368-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="76368-116">Im _nPropID_ -Parameter übernimmt **MakeIconFromBinary** den Eigenschaftenbezeichner einer der Symbol Eigenschaften eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="76368-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="76368-117">Mit dieser Eigenschaftskennung wird ein Symbol erstellt, das in Tabellen Ansichten angezeigt werden kann, die Eigenschaftsspalten für Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="76368-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76368-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76368-118">See also</span></span>



[<span data-ttu-id="76368-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="76368-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

