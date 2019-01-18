---
title: TableDef.ConflictTable-Eigenschaft (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718917"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="4026b-102">TableDef.ConflictTable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4026b-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="4026b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4026b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4026b-p101">Gibt den Name einer Konflikttabelle zurück, die die Datensätze der Datenbank enthält, die bei der Synchronisierung zweier Replikate einen Konflikt ausgelöst haben (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4026b-p101">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only). Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4026b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4026b-106">Syntax</span></span>

<span data-ttu-id="4026b-107">*Ausdruck* . ConflictTable</span><span class="sxs-lookup"><span data-stu-id="4026b-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="4026b-108">*Ausdruck* Ein Ausdruck, der ein **TableDef** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4026b-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4026b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4026b-109">Remarks</span></span>

<span data-ttu-id="4026b-110">Der Rückgabewert ist vom Datentyp **String** mit einer leeren Zeichenfolge (""), wenn es keine Konflikttabelle gibt oder die Datenbank kein Replikat ist.</span><span class="sxs-lookup"><span data-stu-id="4026b-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="4026b-p102">Wenn zwei Benutzer an zwei gesonderten Replikaten Änderungen an demselben Datensatz in der Datenbank vornehmen, können die Änderungen eines Benutzers nicht auf das andere Replikat angewendet werden. Folglich muss der Benutzer, dessen Änderungen fehlschlugen, die Konflikte auflösen.</span><span class="sxs-lookup"><span data-stu-id="4026b-p102">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica. Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="4026b-p103">Konflikte treten auf Datensatzebene auf, nicht zwischen Feldern. Wenn z. B. ein Benutzer das Adressfeld ändert und ein anderer Benutzer das Telefonnummernfeld desselben Datensatzes aktualisiert, wird eine Änderung abgelehnt. Da Konflikte auf der Datensatzebene auftreten, erfolgt die Ablehnung, obwohl die erfolgreiche Änderung und die abgelehnte Änderung kaum zu einem echten Informationskonflikt führen.</span><span class="sxs-lookup"><span data-stu-id="4026b-p103">Conflicts occur at the record level, not between fields. For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected. Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="4026b-p104">Der Synchronisierungsmechanismus verarbeitet die Datensatzkonflikte. Dabei werden Konflikttabellen erstellt, die die Informationen enthalten, die bei einer erfolgreichen Änderung in der Tabelle gespeichert worden wären. Sie können diese Konflikttabellen überprüfen und Zeile für Zeile die erforderlichen Korrekturen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="4026b-p104">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful. You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="4026b-118">Konflikttabellen heißen Tabelle\_Konflikt, wobei Tabelle der ursprüngliche Name der Tabelle ist, auf die maximal zulässige Länge gekürzt.</span><span class="sxs-lookup"><span data-stu-id="4026b-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

