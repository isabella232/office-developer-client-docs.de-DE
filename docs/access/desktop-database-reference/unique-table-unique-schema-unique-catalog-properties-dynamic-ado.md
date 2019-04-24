---
title: Unique Table, Unique Schema, Unique Catalog Dynamic Properties (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313748"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="f901f-102">Unique Table, Unique Schema, Unique Catalog Dynamic Properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="f901f-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="f901f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f901f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f901f-104">Hiermit können Sie Änderungen an einer bestimmten Basistabelle in einem [Recordset](recordset-object-ado.md)-Objekt, das mit einer JOIN-Operation für mehrere Basistabellen erstellt wurde, lückenlos überwachen.</span><span class="sxs-lookup"><span data-stu-id="f901f-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="f901f-105">**Unique Table** gibt den Namen der Basistabelle an, für die Aktualisierungen, Einfügungen und Löschvorgänge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f901f-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="f901f-106">**Unique Schema** gibt das *Schema* oder aber den Namen des Tabellenbesitzers an.</span><span class="sxs-lookup"><span data-stu-id="f901f-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="f901f-107">**Unique Catalog** gibt den *Katalog* oder aber den Namen der Datenbank an, die die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="f901f-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f901f-108">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f901f-108">Settings and return values</span></span>

<span data-ttu-id="f901f-109">Mit diesen Eigenschaften wird ein Wert vom Datentyp **String** festgelegt oder zurückgegeben, der den Namen einer Tabelle, eines Schemas oder eines Katalogs darstellt.</span><span class="sxs-lookup"><span data-stu-id="f901f-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="f901f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f901f-110">Remarks</span></span>

<span data-ttu-id="f901f-p101">Die gewünschte Basistabelle wird durch die Katalog-, Schema- und Tabellennamen eindeutig identifiziert. Wenn die **Unique Table**-Eigenschaft festgelegt ist, werden die Werte der **Unique Schema**- oder **Unique Catalog**-Eigenschaft zum Suchen der Basistabelle verwendet. Es ist vorgesehen, aber nicht erforderlich, dass die **Unique Schema**-Eigenschaft und/oder die **Unique Catalog**-Eigenschaft vor der **Unique Table**-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f901f-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="f901f-p102">Der Primärschlüssel der **Unique Table** -Eigenschaft wird als Primärschlüssel des gesamten **Recordset** -Objekts behandelt. Dieser Schlüssel wird für jede Methode verwendet, die einen Primärschlüssel erfordert.</span><span class="sxs-lookup"><span data-stu-id="f901f-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="f901f-p103">Wenn **Unique Table** festgelegt ist, betrifft die [Delete](delete-method-ado-recordset.md)-Methode nur die genannte Tabelle. Die Methoden [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) und [UpdateBatch](updatebatch-method-ado.md) betreffen alle zugrunde liegenden entsprechenden Basistabellen des **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f901f-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="f901f-p104">**Unique Table** muss vor benutzerdefinierten Neusynchronisierungen angegeben werden. Wenn **Unique Table** nicht angegegben ist, hat der [Resync Command](resync-command-property-dynamic-ado.md)-Eigenschaft keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="f901f-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="f901f-120">Ein Laufzeitfehler wird erzeugt, wenn eine eindeutige Basistabelle nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="f901f-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="f901f-121">Diese dynamischen Eigenschaften werden alle an die **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts angefügt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f901f-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

