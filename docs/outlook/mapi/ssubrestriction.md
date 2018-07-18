---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795624"
---
# <a name="ssubrestriction"></a><span data-ttu-id="fd58f-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="fd58f-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="fd58f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd58f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd58f-105">Eine untergeordnete Objekt Beschränkung der verwendet wird, um die Zeilen der Anlage einer Nachricht oder ein Empfänger Tabelle Filtern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fd58f-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd58f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fd58f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd58f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd58f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="fd58f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="fd58f-108">Members</span></span>

 <span data-ttu-id="fd58f-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="fd58f-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="fd58f-110">Typ des untergeordneten Objekts als Ziel für die Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="fd58f-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="fd58f-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fd58f-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="fd58f-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="fd58f-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="fd58f-113">Wenden Sie die Einschränkung auf Empfänger einer Nachricht-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd58f-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="fd58f-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="fd58f-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="fd58f-115">Die Beschränkung auf eine Nachricht Anlagentabelle anwenden.</span><span class="sxs-lookup"><span data-stu-id="fd58f-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="fd58f-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="fd58f-116">**lpRes**</span></span>
  
> <span data-ttu-id="fd58f-117">Zeiger auf eine [SRestriction](srestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fd58f-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fd58f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd58f-118">Remarks</span></span>

<span data-ttu-id="fd58f-119">Untergeordnete Objekt Einschränkungen werden durch die alle Tabellen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd58f-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="fd58f-120">In der Regel nur Ordner Inhalt Tabellen und die Ergebnisse Suchordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd58f-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="fd58f-121">Beispielsweise werden Einschränkungen untergeordneten Objekts verwendet, um eine Nachricht zu suchen, die einen bestimmten Typ Anlage oder ein Empfänger hat.</span><span class="sxs-lookup"><span data-stu-id="fd58f-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="fd58f-122">Wenn eine Implementierung der untergeordneten Objekts Einschränkungen nicht unterstützt werden, gibt die [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md) Methoden MAPI_E_TOO_COMPLEX zurück.</span><span class="sxs-lookup"><span data-stu-id="fd58f-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="fd58f-123">Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="fd58f-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd58f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd58f-124">See also</span></span>



[<span data-ttu-id="fd58f-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fd58f-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="fd58f-126">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fd58f-126">MAPI Structures</span></span>](mapi-structures.md)

