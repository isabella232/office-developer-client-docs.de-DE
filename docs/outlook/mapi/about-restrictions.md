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
ms.openlocfilehash: 003655354ecac8e2910b3e6851da32c28ce31cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586454"
---
# <a name="about-restrictions"></a><span data-ttu-id="0861b-103">Informationen zu Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="0861b-103">About Restrictions</span></span>

  
  
<span data-ttu-id="0861b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0861b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0861b-105">Eine Einschränkung ist eine Möglichkeit zur Begrenzung der Anzahl der Zeilen in einer Ansicht, um nur die Zeilen mit Werten für Spalten, die bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0861b-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="0861b-106">Es gibt viele verschiedene Möglichkeiten für die Verwendung von Einschränkungen mit Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0861b-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="0861b-107">Clientanwendungen können Einschränkungen, beispielsweise zum Filtern einer Inhaltstabelle für Nachrichten, die von einer bestimmten Person, Zeilen suchen, die entweder eine Eigenschaft nicht unterstützt, oder eine Eigenschaft auf einen bestimmten Wert festgelegt haben, oder für doppelte Empfänger innerhalb einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0861b-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="0861b-108">Die [Methode IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable](imapitable-findrow.md) Methoden werden verwendet, um Einschränkungen für eine Tabelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0861b-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="0861b-109">**Restrict** gilt die Einschränkung für die Tabelle ohne Abrufen von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="0861b-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="0861b-110">Um nur die Zeilen abrufen, die die Einschränkung entsprechen, ist ein nachfolgender Aufruf [IMAPITable::QueryRows](imapitable-queryrows.md) oder einer ähnlichen Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0861b-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="0861b-111">**FindRow** gilt die Einschränkung und ruft die erste Zeile in der Tabelle, die den Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="0861b-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="0861b-112">**FindRow** wendet die temporäre Einschränkung, die nur für die Dauer des Anrufs, vorhanden ist, **Restrict** eine permanente Beschränkung gilt.</span><span class="sxs-lookup"><span data-stu-id="0861b-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="0861b-113">Einige Clients können erstellen Sie eine Einschränkung von Spalten, die nicht in der aktuellen Spalte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="0861b-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="0861b-114">Unterstützung für diese Beschränkung ist optional und Implementierer Tabelle, die sie unterstützen Hinzufügen eines Werts, insbesondere für Inhalt Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0861b-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="0861b-115">Tabelle-Implementierung, die nicht unterstützen kann den Wert MAPI_E_TOO_COMPLEX aus einen Anruf **Restrict** oder den Wert des MAPI_E_NOT_FOUND aus einen Anruf **FindRow** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0861b-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="0861b-116">Clients sollten beachten, dass, auch wenn der Anbieter das Einschränkungen auf Spalten in der aktuellen Spalte Gruppe nicht unterstützt, sie eine bessere Leistung insgesamt erhalten durch Angeben der Spalten, die sie in ihre Einschränkungen mit [IMAPITable::SetColumns](imapitable-setcolumns.md) verwenden möchten .</span><span class="sxs-lookup"><span data-stu-id="0861b-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0861b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0861b-117">See also</span></span>



[<span data-ttu-id="0861b-118">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="0861b-118">MAPI Tables</span></span>](mapi-tables.md)

