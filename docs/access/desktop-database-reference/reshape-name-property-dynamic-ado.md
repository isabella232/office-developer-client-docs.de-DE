---
title: Reshape Name (dynamische Eigenschaft) (ADO)
TOCTitle: Reshape Name Property--Dynamic (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bebdec8bdc68724522331714052a0079f75b28e3
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603168"
---
# <a name="reshape-name-property--dynamic-ado"></a>Reshape Name (dynamische Eigenschaft) (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt einen Namen für das [Recordset](recordset-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="return-values"></a>Rückgabewert
=======
## <a name="return-values"></a>Rückgabewerte
>>>>>>> master

Gibt einen Wert vom Datentyp **String** zurück, der den Namen des **Recordset** -Objekts darstellt.

## <a name="remarks"></a>Hinweise

Namen bleiben für die Dauer der Verbindung oder bis zum Schließen des **Recordset** -Objekts erhalten.

Die **Reshape Name** -Eigenschaft ist hauptsächlich zum Verwenden mit dem Neustrukturierungsfeature des Dienstanbieters [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) vorgesehen. Namen müssen eindeutig sein, damit sie für die Neustrukturierung verwendet werden.

Diese Eigenschaft ist schreibgeschützt, kann aber indirekt festgelegt werden, wenn ein Recordset-Objekt erstellt wird. Wenn z. B. mit einer Klausel eines SHAPE-Befehls ein Recordset-Objekt erstellt und der Aliasname mit dem AS-Schlüsselwort erteilt wird, dann wird der Alias der Reshape Name-Eigenschaft zugewiesen. Wenn kein Alias deklariert wird, wird der Reshape Name-Eigenschaft ein vom Datenstrukturierungsdienst generierter eindeutiger Name zugewiesen. Falls der Aliasname mit dem Namen eines vorhandenen Recordset-Objekts identisch ist, werden die beiden Recordset-Objekte erst neustrukturiert, wenn eines der beiden Objekte freigegeben wird. Das Standardverhalten kann geändert werden, indem Sie die Unique Reshape Names-Eigenschaft (siehe "Microsoft Data Shaping Dienst für OLE DB") für die ADO-Verbindung auf TRUE festlegen. Dadurch kann der Datenstrukturierungsdienst bei Bedarf vom Benutzer zugewiesene Namen ändern, um die Eindeutigkeit der Namen sicherzustellen.

Verwenden Sie die **Reshape Name** -Eigenschaft, wenn Sie in einem SHAPE-Befehl auf ein **Recordset** -Objekt verweisen möchten oder wenn Sie den Namen des Objekts nicht kennen, weil es vom Datenstrukturierungsdienst generiert wurde. In diesem Fall können Sie einen SHAPE-Befehl generieren, indem Sie den Befehl mit der von der **Reshape Name** -Eigenschaft zurückgegebenen Zeichenfolge verketten.

**Reshape Name** ist eine dynamische Eigenschaft, die an die **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.
