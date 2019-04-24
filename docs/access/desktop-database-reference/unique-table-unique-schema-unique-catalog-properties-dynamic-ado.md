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
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>Unique Table, Unique Schema, Unique Catalog Dynamic Properties (ADO)


**Gilt für**: Access 2013, Office 2013

Hiermit können Sie Änderungen an einer bestimmten Basistabelle in einem [Recordset](recordset-object-ado.md)-Objekt, das mit einer JOIN-Operation für mehrere Basistabellen erstellt wurde, lückenlos überwachen.

  - **Unique Table** gibt den Namen der Basistabelle an, für die Aktualisierungen, Einfügungen und Löschvorgänge zulässig sind.

  - **Unique Schema** gibt das *Schema* oder aber den Namen des Tabellenbesitzers an.

  - **Unique Catalog** gibt den *Katalog* oder aber den Namen der Datenbank an, die die Tabelle enthält.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit diesen Eigenschaften wird ein Wert vom Datentyp **String** festgelegt oder zurückgegeben, der den Namen einer Tabelle, eines Schemas oder eines Katalogs darstellt.

## <a name="remarks"></a>Bemerkungen

Die gewünschte Basistabelle wird durch die Katalog-, Schema- und Tabellennamen eindeutig identifiziert. Wenn die **Unique Table**-Eigenschaft festgelegt ist, werden die Werte der **Unique Schema**- oder **Unique Catalog**-Eigenschaft zum Suchen der Basistabelle verwendet. Es ist vorgesehen, aber nicht erforderlich, dass die **Unique Schema**-Eigenschaft und/oder die **Unique Catalog**-Eigenschaft vor der **Unique Table**-Eigenschaft festgelegt werden.

Der Primärschlüssel der **Unique Table** -Eigenschaft wird als Primärschlüssel des gesamten **Recordset** -Objekts behandelt. Dieser Schlüssel wird für jede Methode verwendet, die einen Primärschlüssel erfordert.

Wenn **Unique Table** festgelegt ist, betrifft die [Delete](delete-method-ado-recordset.md)-Methode nur die genannte Tabelle. Die Methoden [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) und [UpdateBatch](updatebatch-method-ado.md) betreffen alle zugrunde liegenden entsprechenden Basistabellen des **Recordset** -Objekts.

**Unique Table** muss vor benutzerdefinierten Neusynchronisierungen angegeben werden. Wenn **Unique Table** nicht angegegben ist, hat der [Resync Command](resync-command-property-dynamic-ado.md)-Eigenschaft keine Auswirkungen.

Ein Laufzeitfehler wird erzeugt, wenn eine eindeutige Basistabelle nicht gefunden werden kann.

Diese dynamischen Eigenschaften werden alle an die **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts angefügt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

