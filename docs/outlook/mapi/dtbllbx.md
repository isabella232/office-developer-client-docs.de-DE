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
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438568"
---
# <a name="dtbllbx"></a><span data-ttu-id="fd61d-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="fd61d-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="fd61d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd61d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd61d-105">Beschreibt eine Liste, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd61d-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd61d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fd61d-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd61d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fd61d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="fd61d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="fd61d-108">Members</span></span>

 <span data-ttu-id="fd61d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fd61d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="fd61d-110">Bitmaske der Flags, die verwendet werden, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fd61d-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="fd61d-111">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fd61d-111">The following flags can be set:</span></span>
    
<span data-ttu-id="fd61d-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="fd61d-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="fd61d-113">Es sollte keine horizontale Bildlaufleiste mit der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd61d-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="fd61d-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="fd61d-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="fd61d-115">Es sollte keine vertikale Bildlaufleiste mit der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd61d-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="fd61d-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="fd61d-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="fd61d-117">Property-Tag für eine Eigenschaft eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="fd61d-117">Property tag for a property of any type.</span></span> <span data-ttu-id="fd61d-118">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableTable** -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fd61d-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="fd61d-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="fd61d-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="fd61d-120">Property-Tag für eine Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe eines **openProperty** -Aufrufs geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd61d-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="fd61d-121">Die Anzahl der Spalten, die die Tabelle aufweisen sollte, hängt davon ab, ob es sich bei der Liste um eine einzelne oder mehrere Auswahllisten handelt.</span><span class="sxs-lookup"><span data-stu-id="fd61d-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="fd61d-122">Wenn das **ulPRSetProperty** -Element auf **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) festgelegt ist, ermöglicht die Liste die Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="fd61d-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd61d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd61d-123">Remarks</span></span>

<span data-ttu-id="fd61d-124">Eine **DTBLLBX** -Struktur beschreibt eine Liste ein Steuerelement, das zum Anzeigen mehrerer Elemente verwendet wird, und lassen Sie einen Benutzer eines oder mehrere der Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd61d-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="fd61d-125">Das **ulPRSetProperty** -Element und das **ulPRTableName** -Element arbeiten zusammen; Wenn ein Wert aus der Tabelle ausgewählt wird, wird er zurück in **ulPRSetProperty** geschrieben, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="fd61d-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="fd61d-126">Der Flags-Wert gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd61d-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="fd61d-127">Der Standardwert ist, dass bei Bedarf Typen von Bildlaufleisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd61d-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="fd61d-128">Dienstanbieter können festlegen, dass MAPI_NO_HBAR eine horizontale Bildlaufleiste und MAPI_NO_VBAR zum unterdrücken einer vertikalen Bildlaufleiste unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="fd61d-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="fd61d-129">Die beiden Elemente des Property-Tags arbeiten zusammen, um Werte in der Liste anzuzeigen und entsprechende Eigenschaften festzulegen, wenn ein Element in der Liste ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fd61d-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="fd61d-130">Wenn die Liste von MAPI zuerst angezeigt wird, wird die OpenProperty \*\*\*\* -Methode der **IMAPIProp** -Implementierung aufgerufen, um die im **ulPRTableName** -Element identifizierte Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd61d-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="fd61d-131">Die Anzahl der Spalten in der Tabelle hängt vom Wert des **ulPRSetProperty** -Elements ab.</span><span class="sxs-lookup"><span data-stu-id="fd61d-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="fd61d-132">Wenn **ulPRSetProperty** auf **PR_NULL**festgelegt ist, handelt es sich bei der Liste um eine Liste mit mehreren Auswahlen, die auf einem Objekt mit Empfängern wie einem Adressbuchcontainer, einer Empfängertabelle für eine Nachricht oder einer Tabelle mit Verteilerlisten Inhalten basiert.</span><span class="sxs-lookup"><span data-stu-id="fd61d-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="fd61d-133">Eine Tabelle für eine Liste mit mehreren Auswahlen muss die folgenden Spalten enthalten:</span><span class="sxs-lookup"><span data-stu-id="fd61d-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="fd61d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fd61d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="fd61d-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fd61d-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="fd61d-136">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fd61d-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="fd61d-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und maximal fünf weitere Zeichenfolgeneigenschaften können auch mit den drei erforderlichen Spalten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd61d-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="fd61d-138">Wenn das **ulPRSetProperty** -Element nicht auf **PR_NULL**festgelegt ist, handelt es sich bei der Liste um eine einzelne Auswahlliste.</span><span class="sxs-lookup"><span data-stu-id="fd61d-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="fd61d-139">Der Anfangswert von **ulPRSetProperty** bestimmt die erste ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd61d-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="fd61d-140">Wenn ein Benutzer eine der Zeilen auswählt, wird das **ulPRSetProperty** -Element auf den ausgewählten Wert festgelegt, und dieser Wert wird in die Implementierung der Property-Schnittstelle mit einem Aufruf von [IMAPIProp::](imapiprop-setprops.md)SetProps zurückgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="fd61d-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="fd61d-141">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fd61d-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="fd61d-142">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fd61d-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd61d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd61d-143">See also</span></span>



[<span data-ttu-id="fd61d-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="fd61d-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="fd61d-145">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fd61d-145">MAPI Structures</span></span>](mapi-structures.md)

