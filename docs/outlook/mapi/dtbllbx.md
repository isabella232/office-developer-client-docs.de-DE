---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569764"
---
# <a name="dtbllbx"></a><span data-ttu-id="7d600-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="7d600-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="7d600-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d600-105">Beschreibt eine Liste, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d600-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d600-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7d600-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d600-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d600-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="7d600-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7d600-108">Members</span></span>

 <span data-ttu-id="7d600-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7d600-109">**ulFlags**</span></span>
  
> <span data-ttu-id="7d600-110">Bitmaske von Flags, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7d600-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="7d600-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7d600-111">The following flags can be set:</span></span>
    
<span data-ttu-id="7d600-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="7d600-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="7d600-113">Keine horizontale Bildlaufleiste angezeigt, die mit der Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d600-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="7d600-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="7d600-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="7d600-115">Keine vertikale Bildlaufleiste angezeigt, die mit der Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d600-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="7d600-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="7d600-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="7d600-117">Eigenschaftentag für eine Eigenschaft eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="7d600-117">Property tag for a property of any type.</span></span> <span data-ttu-id="7d600-118">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableTable** -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7d600-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="7d600-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="7d600-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="7d600-120">Rufen Sie die Eigenschaftentag für ein Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe einer **OpenProperty** geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="7d600-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="7d600-121">Die Anzahl der Spalten, die die Tabelle verfügen soll, hängt davon ab, ob die Liste eine einzelne oder mehrere Auswahlliste enthält.</span><span class="sxs-lookup"><span data-stu-id="7d600-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="7d600-122">Wenn das Element **UlPRSetProperty** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt ist, können die Liste für die Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="7d600-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d600-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7d600-123">Remarks</span></span>

<span data-ttu-id="7d600-124">Eine Struktur **DTBLLBX** beschreibt eine Liste ein Steuerelement, das verwendet wird, um mehrere Elemente anzeigen, und lassen Sie einen Benutzer ein oder mehrere Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="7d600-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="7d600-125">Die **UlPRSetProperty** und **UlPRTableName** arbeiten zusammen, Wenn ein Wert aus der Tabelle ausgewählt ist, wird sie wieder in **UlPRSetProperty** geschrieben, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7d600-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="7d600-126">Der Wert des Flags gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d600-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="7d600-127">Die Standardmethode ist auf Typen von Rollen haben, die Bildlaufleisten angezeigt werden, wenn es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7d600-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="7d600-128">Dienstanbieter können MAPI_NO_HBAR unterdrückt werden, eine horizontale Bildlaufleiste und MAPI_NO_VBAR unterdrückt werden, eine vertikale Bildlaufleiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="7d600-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="7d600-129">Die zwei-Eigenschaft Tag Member arbeiten zusammen, um Werte in der Liste anzeigen und die entsprechenden Eigenschaften festgelegt werden, wenn ein Element in der Liste ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7d600-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="7d600-130">Wenn MAPI zuerst der Liste angezeigt wird, wird die **IMAPIProp** Implementierung **OpenProperty** -Methode zum Abrufen der Tabelle im **UlPRTableName** -Member identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7d600-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="7d600-131">Die Anzahl der Spalten in der Tabelle, hängt von den Wert des Elements **UlPRSetProperty** ab.</span><span class="sxs-lookup"><span data-stu-id="7d600-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="7d600-132">Wenn **UlPRSetProperty** auf **PR_NULL**festgelegt ist, wird die Liste eine mehrere Auswahlliste basierend auf ein Objekt, Empfänger, wie ein Adressbuchcontainer, Tabellengröße Empfänger für eine Nachricht oder einer Verteilergruppe Liste Inhalt-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="7d600-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="7d600-133">Eine Tabelle für eine mehrere Auswahlliste muss die folgenden Spalten enthalten:</span><span class="sxs-lookup"><span data-stu-id="7d600-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="7d600-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d600-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="7d600-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d600-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="7d600-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d600-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="7d600-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und bis zu fünf Zeichenfolgeneigenschaften andere mehrwertige kann auch mit den drei erforderlichen Spalten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7d600-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="7d600-138">Wenn das Element **UlPRSetProperty** nicht auf **PR_NULL**festgelegt ist, ist die Liste eine einzelne Auswahlliste aus.</span><span class="sxs-lookup"><span data-stu-id="7d600-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="7d600-139">Der Anfangswert der **UlPRSetProperty** bestimmt die zuerst ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="7d600-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="7d600-140">Wenn ein Benutzer eine der Zeilen auswählt, **UlPRSetProperty** Elements auf den ausgewählten Wert festgelegt ist, und dieser Wert wird zurück an die Implementierung der Eigenschaft-Schnittstelle mit einem Aufruf von [IMAPIProp::SetProps](imapiprop-setprops.md)geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d600-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="7d600-141">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7d600-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="7d600-142">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="7d600-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d600-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d600-143">See also</span></span>



[<span data-ttu-id="7d600-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="7d600-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="7d600-145">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7d600-145">MAPI Structures</span></span>](mapi-structures.md)

