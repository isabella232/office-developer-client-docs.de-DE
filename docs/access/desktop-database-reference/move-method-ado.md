---
title: Move-Methode – ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 003c60e021ab773e4540af4739f5cf260048b63b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606562"
---
# <a name="move-method-ado"></a>Move-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Verschiebt die Position des aktuellen Datensatzes in einem [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Recordset*. Move *NumRecords*, *Start*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*NumRecords* |Ein signierter **Long** -Ausdruck, der die Anzahl von Datensätzen angibt, um die die aktuelle Position des Datensatzes verschoben wird.|
|*Start* |Optional. Ein **String** -Wert oder ein **Variant** -Wert, der eine Textmarke ergibt. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.|

## <a name="remarks"></a>HinwBemerkungeneise

Die **Move**-Methode wird für alle **Recordset**-Objekte unterstützt.

Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).

Wenn der **Move-Aufruf** die aktuelle Datensatzposition an einen Punkt vor dem ersten Datensatz verschieben würde, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im Recordset fest ([BOF](bof-eof-properties-ado.md) ist **True**). Beim Versuch, den Datensatz nach hinten zu verschieben, wenn die **BOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.

Wenn die aktuelle Position des Datensatzes beim Aufrufen von **Move** an eine Stelle hinter dem letzten Datensatz verschoben werden würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz in der Datensatzgruppe fest ([EOF](bof-eof-properties-ado.md) ist **True**). Beim Versuch, den Datensatz nach vorn zu verschieben, wenn die **EOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.

Beim Aufrufen der **Move**-Methode aus einem leeren **Recordset**-Objekt wird ein Fehler generiert.

Wenn Sie das Argument *Start* übergeben, ist die Verschiebung relativ zum Datensatz mit dieser Textmarke, wobei davon ausgegangen wird, dass das **Recordset**-Objekt Textmarken unterstützt. Ist es nicht angegeben, ist die Verschiebung relativ zum aktuellen Datensatz.

Falls Sie mithilfe der [CacheSize](cachesize-property-ado.md)-Eigenschaft Datensätze vom Anbieter lokal zwischenspeichern, wird durch das Übergeben eines Arguments *NumRecords*, mit dem die aktuelle Datensatzposition außerhalb der aktuellen Gruppe zwischengespeicherter Datensätze verschoben wird, ADO gezwungen, eine neue Datensatzgruppe ausgehend vom Zieldatensatz abzurufen. Die **CacheSize**-Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.

Ist das **Recordset**-Objekt vorwärtsgerichtet, kann der Benutzer auch ein Argument *NumRecords* übergeben, das kleiner als 0 (Null) ist, wenn sich das Ziel innerhalb der aktuellen Gruppe der zwischengespeicherten Datensätze befindet. Wenn die aktuelle Position des Datensatzes beim Aufrufen von **Move** auf einen Datensatz vor dem ersten zwischengespeicherten Datensatz verschoben wird, tritt ein Fehler auf. Daher können Sie statt einem Anbieter, der nur einen vorwärtsgerichteten Bildlauf unterstützt, einen Datensatzcache verwenden, der einen vollständigen Bildlauf unterstützt. Da zwischengespeicherte Datensätze in den Speicher geladen werden, sollten Sie nur so viele Datensätze wie erforderlich zwischenspeichern. Selbst wenn ein vorwärtsgerichtetes **Recordset**-Objekt rückwärtsgerichtete Verschiebungen dieser Art unterstützt, wird beim Aufrufen der [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode für ein vorwärtsgerichtetes **Recordset**-Objekt ein Fehler generiert.


> [!NOTE]
> [!HINWEIS] Ob in einem vorwärtgerichteten **Recordset** -Objekt rückwärtgerichtete Verschiebungen unterstützt werden, hängt vom Anbieter ab. Wenn der aktuelle Datensatz hinter dem letzten Datensatz im **Recordset** -Objekt positioniert wurde, wird bei einer rückwärtsgerichteten Verschiebung mithilfe von **Move** möglicherweise nicht die richtige aktuelle Position erzielt.


