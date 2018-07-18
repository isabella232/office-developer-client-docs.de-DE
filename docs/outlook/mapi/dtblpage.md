---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86cd30b15402f35e8396dedf6b685050ee4fb45e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791625"
---
# <a name="dtblpage"></a><span data-ttu-id="08713-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="08713-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="08713-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08713-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08713-105">Beschreibt eine Seite, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="08713-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08713-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="08713-106">Header file:</span></span>  <br/> |<span data-ttu-id="08713-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08713-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08713-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="08713-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="08713-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="08713-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="08713-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="08713-110">Members</span></span>

 <span data-ttu-id="08713-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="08713-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="08713-112">Die Position im Speicher der Zeichen Zeichenfolge Beschriftung für die Registerkarte Seite.</span><span class="sxs-lookup"><span data-stu-id="08713-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="08713-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="08713-113">**ulFlags**</span></span>
  
> <span data-ttu-id="08713-114">Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabelName** Member.</span><span class="sxs-lookup"><span data-stu-id="08713-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="08713-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="08713-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="08713-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08713-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="08713-117">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="08713-117">The label is in Unicode format.</span></span> <span data-ttu-id="08713-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="08713-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="08713-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="08713-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="08713-120">Die Position im Arbeitsspeicher einer Zeichenfolge, die im Abschnitt **[Help File Mappings]** in die Datei MAPISVC identifiziert. INF-Konfigurationsdatei oder 0.</span><span class="sxs-lookup"><span data-stu-id="08713-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="08713-121">Der Dateiname in die Datei MAPISVC angezeigt werden. INF-Abschnitt kann von einem Benutzer verwendet werden, um erweiterte Hilfe für die Seite zugreifen, indem Sie auf die Schaltfläche **Hilfe** klicken, im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="08713-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="08713-122">Weitere Informationen zu den Einträgen in der Datei MAPISVC. INF-Datei, finden Sie unter [File Format der Datei MAPISVC. INF-Datei](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="08713-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="08713-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="08713-123">**ulContext**</span></span>
  
> <span data-ttu-id="08713-124">Ein eindeutiger Bezeichner für die Seite in der Zeichenfolge, die durch das **UlbLpszComponent** -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="08713-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="08713-125">Das Element **UlbLpszComponent** und der **UlContext** Member müssen beide ungleich NULL für die Schaltfläche **Hilfe** zu sein.</span><span class="sxs-lookup"><span data-stu-id="08713-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="08713-126">Wenn dieser Bezeichner 0 (null ist) und die Komponente Zeichenfolge NULL ist, ist keine Hilfe mit der Seite verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="08713-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08713-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08713-127">Remarks</span></span>

<span data-ttu-id="08713-128">Eine Struktur **DTBLPAGE** beschreibt eine Seite ein Steuerelement, das verwendet wird, um mehrere zugehörige Dialogfelder zu trennen.</span><span class="sxs-lookup"><span data-stu-id="08713-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="08713-129">In der Regel werden diese Dialogfelder Eigenschaftenseiten für die Konfiguration, Nachricht oder Empfänger Optionen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="08713-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="08713-130">Durch Klicken auf die Registerkarte, kann der Benutzer von einem Arbeitsblatt wechseln.</span><span class="sxs-lookup"><span data-stu-id="08713-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="08713-131">Die Komponente Zeichenfolge und Kontext-ID finden Sie Informationen, ob erweiterte Hilfe für die Seite verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="08713-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="08713-132">Wenn erweiterte Hilfe verfügbar ist, bietet die Komponente Zeichenfolge und Kontext-ID Informationen dazu, wie Sie darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="08713-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="08713-133">Die Komponente Zeichenfolge ordnet der Hilfedatei. die Kontext-ID wird die ursprüngliche Hilfethema zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="08713-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="08713-134">Wenn die Kontext-ID 0 (null ist) und die Komponente Zeichenfolge NULL ist, ist die erweiterte Hilfe nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08713-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="08713-135">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="08713-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="08713-136">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="08713-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08713-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08713-137">See also</span></span>



[<span data-ttu-id="08713-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="08713-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="08713-139">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="08713-139">MAPI Structures</span></span>](mapi-structures.md)

