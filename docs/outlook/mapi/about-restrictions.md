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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322120"
---
# <a name="about-restrictions"></a><span data-ttu-id="1c776-103">Informationen zu Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="1c776-103">About Restrictions</span></span>

  
  
<span data-ttu-id="1c776-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c776-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c776-105">Eine Einschränkung ist eine Möglichkeit, um die Anzahl der Zeilen in einer Ansicht auf die Zeilen mit Werten für Spalten zu begrenzen, die bestimmten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1c776-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="1c776-106">Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen mit Tabellen.</span><span class="sxs-lookup"><span data-stu-id="1c776-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="1c776-107">Client Anwendungen können Einschränkungen verwenden, um beispielsweise eine Inhaltstabelle für Nachrichten zu filtern, die von einer bestimmten Person gesendet werden, nach Zeilen zu suchen, die keine Eigenschaft unterstützen oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder um nach doppelten Empfängern in einem Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1c776-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="1c776-108">Die [IMAPITable:: Restrict](imapitable-restrict.md) -und [IMAPITable:: FindRow](imapitable-findrow.md) -Methoden werden verwendet, um Einschränkungen für eine Tabelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1c776-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="1c776-109">**Restrict** wendet die Einschränkung auf die Tabelle an, ohne Zeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1c776-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="1c776-110">Um nur die Zeilen abzurufen, die der Einschränkung entsprechen, ist ein nach folgender Aufruf von [IMAPITable:: QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c776-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="1c776-111">**FindRow** wendet die Einschränkung an und ruft die erste Zeile in der Tabelle ab, die den Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="1c776-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="1c776-112">**FindRow** wendet eine temporäre Einschränkung an, die nur für die Dauer des Anrufs existiert, wohingegen **Restrict** eine dauerhaftere Einschränkung anwendet.</span><span class="sxs-lookup"><span data-stu-id="1c776-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="1c776-113">Einige Clients können eine Einschränkung mithilfe von Spalten erstellen, die nicht in der aktuellen Spaltengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1c776-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="1c776-114">Die Unterstützung einer solchen Einschränkung ist optional, und Tabellen Implementierer, die Sie unterstützen, fügen einen Wert hinzu, insbesondere für Inhaltstabellen.</span><span class="sxs-lookup"><span data-stu-id="1c776-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="1c776-115">Tabellen Implementierer, die Sie nicht unterstützen, können den MAPI_E_TOO_COMPLEX-Wert aus einem **Restrict** -Aufruf oder aus dem MAPI_E_NOT_FOUND-Wert eines **FindRow** -Aufrufs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1c776-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="1c776-116">Clients sollten beachten, dass auch dann, wenn der Anbieter Einschränkungen für Spalten unterstützt, die nicht in der aktuellen Spaltengruppe enthalten sind, eine bessere Leistung erzielt werden, indem die Spalten angegeben werden, die Sie in ihren Einschränkungen mit [IMAPITable::](imapitable-setcolumns.md) SetColumns verwenden möchten. .</span><span class="sxs-lookup"><span data-stu-id="1c776-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1c776-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c776-117">See also</span></span>



[<span data-ttu-id="1c776-118">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="1c776-118">MAPI Tables</span></span>](mapi-tables.md)

