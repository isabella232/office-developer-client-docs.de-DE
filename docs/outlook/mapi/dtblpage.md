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
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340117"
---
# <a name="dtblpage"></a><span data-ttu-id="6a30a-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6a30a-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="6a30a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a30a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a30a-105">Beschreibt eine Registerkartenseite, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6a30a-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a30a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6a30a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a30a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6a30a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6a30a-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="6a30a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="6a30a-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="6a30a-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="6a30a-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="6a30a-110">Members</span></span>

 <span data-ttu-id="6a30a-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="6a30a-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="6a30a-112">Position im Speicher der Zeichenfolgenbezeichnung für die Registerkarte Seite.</span><span class="sxs-lookup"><span data-stu-id="6a30a-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="6a30a-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6a30a-113">**ulFlags**</span></span>
  
> <span data-ttu-id="6a30a-114">Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabelName** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6a30a-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="6a30a-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6a30a-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="6a30a-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a30a-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6a30a-117">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6a30a-117">The label is in Unicode format.</span></span> <span data-ttu-id="6a30a-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6a30a-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="6a30a-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="6a30a-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="6a30a-120">Position im Speicher einer Zeichenfolge, die den Abschnitt **[Hilfedatei Zuordnungen]** im Mapisvc identifiziert. INF-Konfigurationsdatei oder 0.</span><span class="sxs-lookup"><span data-stu-id="6a30a-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="6a30a-121">Der Dateiname, der im MAPISVC angezeigt wird. Der Abschnitt INF kann von Benutzern verwendet werden, um auf die erweiterte Hilfe für die Registerkartenseite zuzugreifen, indem Sie im Dialogfeld auf die Schaltfläche " **Hilfe** " klicken.</span><span class="sxs-lookup"><span data-stu-id="6a30a-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="6a30a-122">Weitere Informationen zu den Einträgen in MAPISVC. INF finden Sie unter [Datei Format von MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="6a30a-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="6a30a-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="6a30a-123">**ulContext**</span></span>
  
> <span data-ttu-id="6a30a-124">Ein eindeutiger Bezeichner für die Registerkartenseite in der vom **ulbLpszComponent** -Element definierten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6a30a-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="6a30a-125">Das **ulbLpszComponent** -Element und das **ulContext** -Element müssen beide ungleich NULL sein, damit die Schaltfläche " **Hilfe** " funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6a30a-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="6a30a-126">Wenn dieser Bezeichner NULL ist und die Komponenten Zeichenfolge NULL ist, ist der Seite keine Hilfe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6a30a-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6a30a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a30a-127">Remarks</span></span>

<span data-ttu-id="6a30a-128">Eine **DTBLPAGE** -Struktur beschreibt ein Steuerelement mit Registerkarten, das zum Trennen mehrerer verwandter Dialogfelder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a30a-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="6a30a-129">In der Regel sind diese Dialogfelder Eigenschaftenblätter zum Anzeigen von Konfigurations-, Nachrichten-oder Empfängeroptionen.</span><span class="sxs-lookup"><span data-stu-id="6a30a-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="6a30a-130">Durch Klicken auf die Registerkarte kann der Benutzer von einem Blatt zu einem anderen wechseln.</span><span class="sxs-lookup"><span data-stu-id="6a30a-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="6a30a-131">Die Komponenten Zeichenfolge und die Kontext-ID enthalten Informationen darüber, ob die erweiterte Hilfe für die Registerkartenseite verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a30a-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="6a30a-132">Wenn die erweiterte Hilfe verfügbar ist, enthält die Komponenten Zeichenfolge und die Kontext-ID Informationen dazu, wie Sie darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6a30a-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="6a30a-133">Die Komponenten Zeichenfolge wird der Hilfedatei zugeordnet; der Kontextbezeichner wird dem anfänglichen Hilfethema zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6a30a-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="6a30a-134">Wenn der Kontextbezeichner NULL ist und die Komponenten Zeichenfolge NULL ist, ist die erweiterte Hilfe nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a30a-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="6a30a-135">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6a30a-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6a30a-136">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="6a30a-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a30a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a30a-137">See also</span></span>



[<span data-ttu-id="6a30a-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6a30a-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="6a30a-139">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6a30a-139">MAPI Structures</span></span>](mapi-structures.md)

