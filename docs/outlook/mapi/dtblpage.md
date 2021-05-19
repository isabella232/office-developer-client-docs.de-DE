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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424000"
---
# <a name="dtblpage"></a><span data-ttu-id="fdbdd-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="fdbdd-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="fdbdd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdbdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdbdd-105">Beschreibt eine Registerkartenseite, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fdbdd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fdbdd-106">Header file:</span></span>  <br/> |<span data-ttu-id="fdbdd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fdbdd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fdbdd-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="fdbdd-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="fdbdd-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="fdbdd-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="fdbdd-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="fdbdd-110">Members</span></span>

 <span data-ttu-id="fdbdd-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="fdbdd-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="fdbdd-112">Position im Arbeitsspeicher der Zeichenzeichenfolgenbeschriftung für die Seitenregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="fdbdd-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fdbdd-113">**ulFlags**</span></span>
  
> <span data-ttu-id="fdbdd-114">Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf das das **ulbLpszLabelName-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="fdbdd-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fdbdd-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="fdbdd-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fdbdd-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fdbdd-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-117">The label is in Unicode format.</span></span> <span data-ttu-id="fdbdd-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="fdbdd-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="fdbdd-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="fdbdd-120">Position im Arbeitsspeicher einer Zeichenzeichenfolge, die **den Abschnitt [Hilfedateizuordnungen]** im MAPISVC identifiziert. INF-Konfigurationsdatei oder 0.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="fdbdd-121">Der Dateiname, der im MAPISVC angezeigt wird. Der ABSCHNITT "INF" kann von einem Benutzer verwendet werden,  um auf die erweiterte Hilfe für die Registerkartenseite zu zugreifen, indem er im Dialogfeld auf die Schaltfläche Hilfe klickt.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="fdbdd-122">Weitere Informationen zu den Einträgen in MAPISVC. INF, siehe [Dateiformat von MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="fdbdd-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="fdbdd-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="fdbdd-123">**ulContext**</span></span>
  
> <span data-ttu-id="fdbdd-124">Ein eindeutiger Bezeichner für die Registerkartenseite in der vom **ulbLpszComponent-Element definierten Zeichenfolge.**</span><span class="sxs-lookup"><span data-stu-id="fdbdd-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="fdbdd-125">Das **ulbLpszComponent-Element** und das **ulContext-Element** müssen beide ungleich Null sein, damit die Schaltfläche **Hilfe** funktioniert.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="fdbdd-126">Wenn dieser Bezeichner null ist und die Komponentenzeichenfolge NULL ist, ist der Seite keine Hilfe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fdbdd-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fdbdd-127">Remarks</span></span>

<span data-ttu-id="fdbdd-128">Eine **DTBLPAGE-Struktur** beschreibt eine Registerkartenseite ein Steuerelement, das zum Trennen mehrerer zugehöriger Dialogfelder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="fdbdd-129">In der Regel handelt es sich bei diesen Dialogfelder um Eigenschaftenblätter zum Anzeigen von Konfigurations-, Nachrichten- oder Empfängeroptionen.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="fdbdd-130">Durch Klicken auf die Registerkarte kann der Benutzer von einem Blatt zu einem anderen wechseln.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="fdbdd-131">Die Komponentenzeichenfolge und der Kontextbezeichner enthalten Informationen dazu, ob die erweiterte Hilfe für die Registerkartenseite verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="fdbdd-132">Wenn erweiterte Hilfe verfügbar ist, enthalten die Komponentenzeichenfolge und der Kontextbezeichner Informationen zum Zugriff darauf.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="fdbdd-133">Die Komponentenzeichenfolge ordnet der Hilfedatei zu. der Kontextbezeichner dem ersten Hilfethema zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="fdbdd-134">Wenn der Kontextbezeichner null und die Komponentenzeichenfolge NULL ist, ist erweiterte Hilfe nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="fdbdd-135">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fdbdd-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="fdbdd-136">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fdbdd-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fdbdd-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdbdd-137">See also</span></span>



[<span data-ttu-id="fdbdd-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="fdbdd-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="fdbdd-139">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fdbdd-139">MAPI Structures</span></span>](mapi-structures.md)

