---
title: MoveRecord-Methode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d5c3abebc80dea7d5871faa7926cf81bdd9a681f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606569"
---
# <a name="moverecord-method-ado"></a>MoveRecord-Methode (ADO)

**Gilt für**: Access 2013, Office 2013
 
Verschiebt die durch einen [Record](record-object-ado.md) dargestellte Entität an einen anderen Speicherort.

## <a name="syntax"></a>Syntax

*Datensatz*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **String**-Wert mit einer URL, die den zu verschiebenden **Record** identifiziert. Wenn *Source* nicht angegeben ist oder eine leere Zeichenfolge angibt, wird das durch diesen **Record** dargestellte Objekt verschoben. Stellt **Record** beispielsweise eine Datei dar, wird der Inhalt der Datei an den durch *Destination* angegebenen Speicherort verschoben.|
|*Ziel* |Optional. Ein **String**-Wert mit einer URL, die den Speicherort angibt, an den *Source* verschoben wird.|
|*UserName* |Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.|
|*Password* |Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.|
|*Options* |Optional. Ein [MoveRecordOptionsEnum](moverecordoptionsenum.md)-Wert, dessen Standardwert **adMoveUnspecified** lautet. Gibt das Verhalten dieser Methode an.|
|*Async* |Optional. Ein **boolescher** Wert, der bei **True** angibt, dass dieser Vorgang asynchron sein soll.|

## <a name="return-value"></a>Rückgabewert

Ein **String**-Wert. In der Regel wird der Wert für *Destination* zurückgegeben. Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.

## <a name="remarks"></a>HinwBemerkungeneise

Die Werte für *Source* und *Destination* dürfen nicht identisch sein, andernfalls tritt ein Laufzeitfehler auf. Mindestens der Server-, Pfad- und Ressourcenname müssen unterschiedlich sein.

Bei Dateien, die mithilfe des Anbieters für Internet Publishing verschoben wurden, aktualisiert diese Methode alle Hypertextlinks in den zu verschiebenden Dateien, sofern keine andere Angabe durch *Options* erfolgt ist. Diese Methode schlägt fehl, wenn *Destination* ein vorhandenes Objekt (z. B. eine Datei oder ein Verzeichnis) identifiziert. Dies gilt nicht, wenn **adMoveOverWrite** angegeben ist.

> [!NOTE]
> Verwenden Sie die Option **adMoveOverWrite** nur nach sorgfältiger Überlegung. Wenn Sie diese Option beispielsweise beim Verschieben einer Datei in ein Verzeichnis angeben, wird das Verzeichnis gelöscht und durch die Datei ersetzt.

Bestimmte Attribute des **Record** -Objekts (z. B. die [ParentURL](parenturl-property-ado.md)-Eigenschaft) werden nicht aktualisiert, nachdem dieser Vorgang abgeschlossen ist. Aktualisieren Sie die Eigenschaften des **Record** -Objekts, indem Sie den **Record** schließen und anschließend mit der URL des Speicherorts, an den die Datei oder das Verzeichnis verschoben wurde, erneut öffnen.

Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, wird der neue Speicherort der verschobenen Datei oder des verschobenen Verzeichnisses nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset** -Objekt, indem Sie es schließen und erneut öffnen.

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


