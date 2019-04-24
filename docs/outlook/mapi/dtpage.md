---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287106"
---
# <a name="dtpage"></a><span data-ttu-id="2dcb8-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="2dcb8-103">DTPAGE</span></span>

  
  
<span data-ttu-id="2dcb8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dcb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dcb8-105">Beschreibt das Dialogfeld, das von der [BuildDisplayTable](builddisplaytable.md) -Funktion aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2dcb8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2dcb8-106">Header file:</span></span>  <br/> |<span data-ttu-id="2dcb8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2dcb8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="2dcb8-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="2dcb8-108">Members</span></span>

 <span data-ttu-id="2dcb8-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="2dcb8-109">**cctl**</span></span>
  
> <span data-ttu-id="2dcb8-110">Die Anzahl der Steuerelemente, auf die durch das **lpctl** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="2dcb8-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="2dcb8-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="2dcb8-112">Zeiger auf den Namen oder ganzzahligen Bezeichner für die Dialogfeldressource.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="2dcb8-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="2dcb8-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="2dcb8-114">Zeiger auf die Zeichenfolge, die im Abschnitt **[Hilfedatei Zuordnungen]** in MAPISVC. inf angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="2dcb8-115">Da sich **lpszComponent** in einer Union mit dem **ulItemID** -Element befindet, verfügt nur einer dieser Member über gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="2dcb8-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="2dcb8-116">**ulItemID**</span></span>
  
> <span data-ttu-id="2dcb8-117">Integer-Ressourcenbezeichner mit einem Wert kleiner oder gleich 65535, aus dem der Name der Hilfedatei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="2dcb8-118">Da sich **ulItemID** in einer Union mit dem **lpszComponent** -Element befindet, verfügt nur einer dieser Member über gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="2dcb8-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="2dcb8-119">**lpctl**</span></span>
  
> <span data-ttu-id="2dcb8-120">Zeiger auf ein Array von [DTCTL](dtctl.md) -Strukturen, eines für jedes Steuerelement auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2dcb8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dcb8-121">Remarks</span></span>

<span data-ttu-id="2dcb8-122">Um die Hilfedatei für die Registerkartenseite zu identifizieren, legen Sie entweder das **lpszComponent** -Element auf eine hart codierte Zeichenfolge oder das **ulItemID** -Element auf einen ganzzahligen Ressourcenbezeichner fest.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="2dcb8-123">Jeder Eintrag im Abschnitt **[Hilfedatei Zuordnungen]** in MAPISVC. INF besteht aus einer Komponenten Zeichenfolge, die nicht länger als 30 Zeichen ist, auf der linken Seite und einem Pfad rechts für die Hilfedatei.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="2dcb8-124">Sowohl **ulItemID** als auch **lpszResourceName** befinden sich im _HINSTANCE_ -Parameter von **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="2dcb8-125">Weitere Informationen finden Sie unter [MAPISVC. Abschnitt "INF [Hilfedatei Zuordnungen]"](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="2dcb8-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="2dcb8-126">Obwohl **BuildDisplayTable** diese Struktur verwendet, um die Anzeigetabelle aus den Steuerelementressourcen zu erstellen, wird die **DTPAGE** -Struktur nie in der Anzeigetabelle selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dcb8-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="2dcb8-127">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2dcb8-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2dcb8-128">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="2dcb8-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dcb8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dcb8-129">See also</span></span>



[<span data-ttu-id="2dcb8-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="2dcb8-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="2dcb8-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="2dcb8-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="2dcb8-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2dcb8-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="2dcb8-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2dcb8-133">MAPI Structures</span></span>](mapi-structures.md)

