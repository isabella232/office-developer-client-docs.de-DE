---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410686"
---
# <a name="dtbllabel"></a><span data-ttu-id="b1125-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="b1125-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="b1125-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1125-105">Beschreibt eine Bezeichnung, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1125-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1125-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b1125-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1125-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1125-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b1125-108">Verwandtes Makro</span><span class="sxs-lookup"><span data-stu-id="b1125-108">Related macro</span></span>  <br/> |[<span data-ttu-id="b1125-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="b1125-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="b1125-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="b1125-110">Members</span></span>

 <span data-ttu-id="b1125-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="b1125-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="b1125-112">Position im Arbeitsspeicher der Zeichenzeichenfolgenbeschriftung.</span><span class="sxs-lookup"><span data-stu-id="b1125-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="b1125-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b1125-113">**ulFlags**</span></span>
  
> <span data-ttu-id="b1125-114">Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf das das **ulbLpszLabelName-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="b1125-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="b1125-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b1125-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="b1125-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1125-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1125-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b1125-117">The label is in Unicode format.</span></span> <span data-ttu-id="b1125-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b1125-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1125-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1125-119">Remarks</span></span>

<span data-ttu-id="b1125-120">Eine **DTBLLABEL-Struktur** beschreibt einen Beschriftungssteuerelementtext, der mit einem anderen Steuerelementtyp angezeigt wird, um diesem Steuerelement Bedeutung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b1125-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="b1125-121">Die meisten Bearbeitungssteuerelemente werden beispielsweise neben Beschriftungen positioniert, um den Benutzer über die Art der eingegebenen Informationen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b1125-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="b1125-122">Einige Steuerelemente, z. B. Gruppenfelder und Optionsfelder, enthalten eigene Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="b1125-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="b1125-123">Die Bezeichnung kann eine Windows, die als Zeichen nach dem ampersand ( ) identifiziert &amp; wird.</span><span class="sxs-lookup"><span data-stu-id="b1125-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="b1125-124">Durch Drücken der Zugriffstaste wird der Fokus im ersten nicht gekennzeichneten, nicht auf diese Bezeichnung folgenden Steuerelement in der Anzeigetabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1125-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="b1125-125">Es gibt keine Unterstützung für mehrstufige Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="b1125-125">There is no support for multiline labels.</span></span> <span data-ttu-id="b1125-126">Das Anzeigen mehrerer Zeilen erfordert mehrere Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="b1125-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="b1125-127">Es ist nicht möglich, eine Bezeichnung als schreibgeschütztes Bearbeitungssteuerelement zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1125-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="b1125-128">Der Unterschied ist, dass ein Bearbeitungssteuerelement ausgewählt und kopiert werden kann, während eine Bezeichnung nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="b1125-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="b1125-129">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b1125-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b1125-130">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b1125-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1125-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1125-131">See also</span></span>



[<span data-ttu-id="b1125-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b1125-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="b1125-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b1125-133">MAPI Structures</span></span>](mapi-structures.md)

