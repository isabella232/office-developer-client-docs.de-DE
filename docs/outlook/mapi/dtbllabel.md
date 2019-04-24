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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287160"
---
# <a name="dtbllabel"></a><span data-ttu-id="fd98e-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="fd98e-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="fd98e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd98e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd98e-105">Beschreibt eine Bezeichnung, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd98e-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd98e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fd98e-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd98e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fd98e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fd98e-108">Zugehöriges Makro</span><span class="sxs-lookup"><span data-stu-id="fd98e-108">Related macro</span></span>  <br/> |[<span data-ttu-id="fd98e-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="fd98e-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="fd98e-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="fd98e-110">Members</span></span>

 <span data-ttu-id="fd98e-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="fd98e-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="fd98e-112">Position im Speicher der Zeichenfolgenbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="fd98e-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="fd98e-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fd98e-113">**ulFlags**</span></span>
  
> <span data-ttu-id="fd98e-114">Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabelName** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fd98e-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="fd98e-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fd98e-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="fd98e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd98e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fd98e-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fd98e-117">The label is in Unicode format.</span></span> <span data-ttu-id="fd98e-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fd98e-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd98e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd98e-119">Remarks</span></span>

<span data-ttu-id="fd98e-120">Eine **DTBLLABEL** -Struktur beschreibt einen Beschriftungssteuerelement Text, der mit einem anderen Steuerelementtyp angezeigt wird, um diesem Steuerelement eine Bedeutung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd98e-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="fd98e-121">Die meisten Bearbeitungssteuerelemente werden beispielsweise neben Bezeichnungen positioniert, um den Benutzer über den Typ der einzugebenden Informationen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="fd98e-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="fd98e-122">Einige Steuerelemente wie Gruppen-und Optionsfelder enthalten eigene Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="fd98e-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="fd98e-123">Die Bezeichnung kann eine Windows-Schnellinfo aufweisen, die als Zeichen nach dem kaufmännischen und (&amp;) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fd98e-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="fd98e-124">Durch Drücken der Tastenkombination wird der Fokus in das erste nicht-Schaltflächen-Steuerelement, das dieser Beschriftung folgt, in der Anzeigetabelle platziert.</span><span class="sxs-lookup"><span data-stu-id="fd98e-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="fd98e-125">Mehrzeilige Beschriftungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd98e-125">There is no support for multiline labels.</span></span> <span data-ttu-id="fd98e-126">Das Anzeigen mehrerer Zeilen erfordert mehrere Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="fd98e-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="fd98e-127">Eine Bezeichnung kann nicht als schreibgeschütztes Bearbeitungssteuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd98e-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="fd98e-128">Der Unterschied besteht darin, dass ein Bearbeitungssteuerelement ausgewählt und kopiert werden kann, während eine Bezeichnung nicht.</span><span class="sxs-lookup"><span data-stu-id="fd98e-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="fd98e-129">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fd98e-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="fd98e-130">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fd98e-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd98e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd98e-131">See also</span></span>



[<span data-ttu-id="fd98e-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="fd98e-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="fd98e-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fd98e-133">MAPI Structures</span></span>](mapi-structures.md)

