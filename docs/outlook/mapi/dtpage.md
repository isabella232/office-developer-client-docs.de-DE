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
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791629"
---
# <a name="dtpage"></a><span data-ttu-id="c7934-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="c7934-103">DTPAGE</span></span>

  
  
<span data-ttu-id="c7934-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7934-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7934-105">Beschreibt das Dialogfeld, die aus einer Tabelle anzeigen von der Funktion [BuildDisplayTable](builddisplaytable.md) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c7934-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7934-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c7934-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7934-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7934-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c7934-108">Members</span><span class="sxs-lookup"><span data-stu-id="c7934-108">Members</span></span>

 <span data-ttu-id="c7934-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="c7934-109">**cctl**</span></span>
  
> <span data-ttu-id="c7934-110">Anzahl der Steuerelemente auf das Element **Lpctl** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c7934-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="c7934-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="c7934-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="c7934-112">Zeiger auf den Namen oder die ganze Zahl Bezeichner für die Feld-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c7934-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="c7934-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="c7934-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="c7934-114">Zeiger auf die Zeichenfolge, die im Abschnitt **[Help File Mappings]** in MAPISVC.INF angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7934-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="c7934-115">Da **LpszComponent** in einer Union mit dem **UlItemID** -Element ist, muss nur einer der folgenden Member gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="c7934-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="c7934-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="c7934-116">**ulItemID**</span></span>
  
> <span data-ttu-id="c7934-117">Ganzzahlige Ressourcenbezeichner mit kleiner oder gleich 65535, von denen der Name der Hilfedatei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7934-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="c7934-118">Da **UlItemID** in einer Union mit dem **LpszComponent** -Element ist, muss nur einer der folgenden Member gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="c7934-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="c7934-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="c7934-119">**lpctl**</span></span>
  
> <span data-ttu-id="c7934-120">Zeiger auf ein Array von [DTCTL](dtctl.md) -Strukturen, einen für jedes Steuerelements auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="c7934-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7934-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7934-121">Remarks</span></span>

<span data-ttu-id="c7934-122">Legen Sie die Hilfedatei für die Seite um zu ermitteln, **LpszComponent** Mitglieds eine hartcodierte Zeichenfolge oder der **UlItemID** Member zu einem ganzzahligen Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7934-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="c7934-123">Jeder Eintrag im Abschnitt **[Help File Mappings]** in MAPISVC. INF-Datei besteht aus einer Zeichenfolge Komponente, die nicht mehr als 30 Zeichen, klicken Sie auf der linken Seite und ein Hilfe Dateipfad auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="c7934-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="c7934-124">**UlItemID** und **LpszResourceName** sind im _hInstance_ -Parameter der **BuildDisplayTable**gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7934-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="c7934-125">Weitere Informationen finden Sie unter [MAPISVC. INF [Hilfe Dateizuordnungen] Abschnitt](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="c7934-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="c7934-126">Obwohl **BuildDisplayTable** diese Struktur verwendet, um der Anzeige-Tabelle aus der Steuerelementressourcen, erstellen die Struktur **DTPAGE** wird nie angezeigt, in der Anzeige Tabelle selbst.</span><span class="sxs-lookup"><span data-stu-id="c7934-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="c7934-127">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c7934-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c7934-128">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c7934-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7934-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7934-129">See also</span></span>



[<span data-ttu-id="c7934-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="c7934-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="c7934-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="c7934-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="c7934-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c7934-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c7934-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c7934-133">MAPI Structures</span></span>](mapi-structures.md)

