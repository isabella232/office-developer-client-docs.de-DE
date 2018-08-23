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
ms.openlocfilehash: 09f0d7988f85a6d6018c45cb64245ab331cda052
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582812"
---
# <a name="dtbllabel"></a><span data-ttu-id="b969c-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="b969c-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="b969c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b969c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b969c-105">Beschreibt eine Beschriftung, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b969c-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b969c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b969c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b969c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b969c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b969c-108">Verwandte Makro</span><span class="sxs-lookup"><span data-stu-id="b969c-108">Related macro</span></span>  <br/> |[<span data-ttu-id="b969c-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="b969c-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="b969c-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="b969c-110">Members</span></span>

 <span data-ttu-id="b969c-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="b969c-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="b969c-112">Die Position im Speicher der Beschriftung Zeichenfolge Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b969c-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="b969c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b969c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="b969c-114">Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabelName** Member.</span><span class="sxs-lookup"><span data-stu-id="b969c-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="b969c-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b969c-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="b969c-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b969c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b969c-117">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b969c-117">The label is in Unicode format.</span></span> <span data-ttu-id="b969c-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b969c-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b969c-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b969c-119">Remarks</span></span>

<span data-ttu-id="b969c-120">Eine Struktur **DTBLLABEL** beschreibt einen Text im Bezeichnungsfeld-Steuerelement, der mit einer anderen Art von Steuerelement, das das Steuerelement Bedeutung hinzugefügt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b969c-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="b969c-121">Beispielsweise sind die meisten Bearbeitungssteuerelemente neben Etiketten informiert den Benutzer über den Typ der Informationen eingegeben werden positioniert.</span><span class="sxs-lookup"><span data-stu-id="b969c-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="b969c-122">Einige Steuerelemente, wie zum Beispiel Gruppenfelder und Optionsfelder, halten Sie ihre eigenen Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="b969c-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="b969c-123">Die Bezeichnung kann einen Windows Accelerator, als das kaufmännische und-Zeichen folgende Zeichen enthalten (&amp;).</span><span class="sxs-lookup"><span data-stu-id="b969c-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="b969c-124">Drücken der Zugriffstaste erhält den Fokus in der ersten Nonlabel, Nonbutton Steuerelement Befolgen dieser Beschriftung in der Tabelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b969c-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="b969c-125">Keine Unterstützung für mehrzeilige Etiketten ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b969c-125">There is no support for multiline labels.</span></span> <span data-ttu-id="b969c-126">Zeigt mehrere Zeilen erfordert mehrere Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="b969c-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="b969c-127">Es ist nicht möglich, eine Beschriftung als einen schreibgeschützten Bearbeitungssteuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="b969c-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="b969c-128">Der Unterschied besteht darin, dass ein Edit-Steuerelement ausgewählt und während eine Bezeichnung kann nicht kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b969c-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="b969c-129">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b969c-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b969c-130">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b969c-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b969c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b969c-131">See also</span></span>



[<span data-ttu-id="b969c-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b969c-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="b969c-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b969c-133">MAPI Structures</span></span>](mapi-structures.md)

