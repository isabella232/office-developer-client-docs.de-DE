---
title: Informationen zu Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433108"
---
# <a name="about-restrictions"></a><span data-ttu-id="711b8-103">Informationen zu Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="711b8-103">About Restrictions</span></span>

  
  
<span data-ttu-id="711b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="711b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="711b8-105">Eine Einschränkung ist eine Möglichkeit, die Anzahl der Zeilen in einer Ansicht auf die Zeilen mit Werten für Spalten zu beschränken, die bestimmten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="711b8-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="711b8-106">Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen für Tabellen.</span><span class="sxs-lookup"><span data-stu-id="711b8-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="711b8-107">Clientanwendungen können Einschränkungen verwenden, z. B. um eine Inhaltstabelle nach Nachrichten zu filtern, die von einer bestimmten Person gesendet wurden, um nach Zeilen zu suchen, die entweder keine Eigenschaft unterstützen oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder um nach doppelten Empfängern in einer Nachricht zu suchen.</span><span class="sxs-lookup"><span data-stu-id="711b8-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="711b8-108">Die [Methoden IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::FindRow](imapitable-findrow.md) werden zum Festlegen von Einschränkungen für eine Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="711b8-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="711b8-109">**Restrict** wendet die Einschränkung auf die Tabelle an, ohne Zeilen abrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="711b8-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="711b8-110">Um nur die Zeilen abzurufen, die die Einschränkung erfüllen, ist ein nachfolgender Aufruf von [IMAPITable::QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="711b8-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="711b8-111">**FindRow** wendet die Einschränkung an und ruft die erste Zeile in der Tabelle ab, die den Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="711b8-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="711b8-112">**FindRow** wendet eine temporäre Einschränkung an, die nur für die Dauer des Anrufs besteht, während **Restrict** eine dauerhaftere Einschränkung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="711b8-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="711b8-113">Einige Clients können eine Einschränkung mithilfe von Spalten erstellen, die sich nicht im aktuellen Spaltensatz befinden.</span><span class="sxs-lookup"><span data-stu-id="711b8-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="711b8-114">Die Unterstützung einer solchen Einschränkung ist optional, und Tabellen implementierer, die sie unterstützen, fügen einen Mehrwert hinzu, insbesondere für Inhaltstabellen.</span><span class="sxs-lookup"><span data-stu-id="711b8-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="711b8-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span><span class="sxs-lookup"><span data-stu-id="711b8-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="711b8-116">Clients sollten beachten, dass auch wenn der Anbieter Einschränkungen für Spalten unterstützt, die nicht im aktuellen Spaltensatz enthalten sind, insgesamt eine bessere Leistung erzielen, indem sie die Spalten angeben, die sie in ihren Einschränkungen mit [IMAPITable::SetColumns](imapitable-setcolumns.md)verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="711b8-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="711b8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="711b8-117">See also</span></span>



[<span data-ttu-id="711b8-118">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="711b8-118">MAPI Tables</span></span>](mapi-tables.md)

