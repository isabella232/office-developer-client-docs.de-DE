---
title: "\"Move\"-Methode - ActiveX Data Objects (ADO)"
TOCTitle: Move Method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c968a53dffbb5463d186c97f4fa36ba5f4dfc29f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883673"
---
# <a name="move-method-ado"></a>Move-Methode (ADO)


**Betrifft**: Access 2013, Office 2013



Verschiebt die Position des aktuellen Datensatzes in einem [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. Verschieben von *NumRecords*, *Starten*

## <a name="parameters"></a>Parameter

  - *NumRecords*

  - Ein signierter **Long** -Ausdruck, der die Anzahl von Datensätzen angibt, um die die aktuelle Position des Datensatzes verschoben wird.

  - *Start*

  - Optional. Ein **String** -Wert oder ein **Variant** -Wert, der eine Textmarke ergibt. Sie können auch einen [BookmarkEnum](bookmarkenum.md)-Wert verwenden.

## <a name="remarks"></a>Hinweise

Die **Move** -Methode wird für alle **Recordset** -Objekte unterstützt.

Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).

Wenn der Anruf **Verschieben** die Position des aktuelle Datensatzes zu einem Zeitpunkt vor dem ersten Datensatz verschoben würde, legt ADO den aktuellen Datensatz an der Position vor dem ersten Datensatz im Recordset-Objekt ([BOF-Eigenschaft](bof-eof-properties-ado.md) ist **True**). Beim Versuch, den Datensatz nach hinten zu verschieben, wenn die **BOF** -Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.

Wenn der Anruf **Verschieben** die Position des aktuelle Datensatzes zu einem Zeitpunkt nach dem letzten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im Recordset-Objekt ([EOF](bof-eof-properties-ado.md) ist **True**). Beim Versuch, den Datensatz nach vorn zu verschieben, wenn die **EOF** -Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.

Beim Aufrufen der **Move** -Methode aus einem leeren **Recordset** -Objekt wird ein Fehler generiert.

Wenn Sie das Argument *Start* übergeben, ist die Verschiebung relativ zum Datensatz mit diesem Lesezeichen, vorausgesetzt, dass das **Recordset** -Objekt Lesezeichen unterstützt. Ist es nicht angegeben, ist die Verschiebung relativ zum aktuellen Datensatz.

Bei Verwendung die [CacheSize](cachesize-property-ado.md) -Eigenschaft auf lokal Cache Datensätze aus der Anbieter auf und übergibt ein *NumRecords* -Argument, das die aktuelle Datensatzposition außerhalb der aktuellen Gruppe der zwischengespeicherten Datensätze verschiebt erzwingt, dass ADO Abrufen einer neuen Gruppe von Datensätzen, Starten aus dem Zieldatensatz. Die **CacheSize** -Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.

Wenn das **Recordset** -Objekt vorwärts nur erfolgt, kann Benutzer weiterhin mit ein Argument *NumRecords* kleiner als 0 (null), übergeben, vorausgesetzt das Ziel innerhalb der aktuellen Gruppe der zwischengespeicherten Einträge ist. Wenn die aktuelle Position des Datensatzes beim Aufrufen von **Move** auf einen Datensatz vor dem ersten zwischengespeicherten Datensatz verschoben wird, tritt ein Fehler auf. Daher können Sie statt einem Anbieter, der nur einen vorwärtsgerichteten Bildlauf unterstützt, einen Datensatzcache verwenden, der einen vollständigen Bildlauf unterstützt. Da zwischengespeicherte Datensätze in den Speicher geladen werden, sollten Sie nur so viele Datensätze wie erforderlich zwischenspeichern. Selbst wenn ein vorwärtsgerichtetes **Recordset** -Objekt rückwärtsgerichtete Verschiebungen dieser Art unterstützt, wird beim Aufrufen der [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode für ein vorwärtsgerichtetes **Recordset** -Objekt ein Fehler generiert.


> [!NOTE]
> [!HINWEIS] Ob in einem vorwärtgerichteten **Recordset** -Objekt rückwärtgerichtete Verschiebungen unterstützt werden, hängt vom Anbieter ab. Wenn der aktuelle Datensatz hinter dem letzten Datensatz im **Recordset** -Objekt positioniert wurde, wird bei einer rückwärtsgerichteten Verschiebung mithilfe von **Move** möglicherweise nicht die richtige aktuelle Position erzielt.


