---
title: Command-Objekt (ADO)
TOCTitle: Command object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3382c83f076c796dde36e0a1a0b84f3972a32a87
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618504"
---
# <a name="command-object-ado"></a>Command-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Definiert einen spezifischen Befehl, den Sie in einer Datenquelle ausführen wollen.

## <a name="remarks"></a>Bemerkungen

Mit einem **Command** -Objekt können Sie eine Datenbank abfragen und Datensätze in einem [Recordset](recordset-object-ado.md)-Objekt zurückgeben, einen Massenvorgang ausführen oder die Struktur einer Datenbank ändern. Abhängig von der Funktionalität des Anbieters wird von einigen **Command** -Auflistungen, -Methoden oder -Eigenschaften möglicherweise ein Fehler erzeugt.

Die Auflistungen, Methoden und Eigenschaften eines **Command** -Objekts ermöglichen Folgendes:

  - Festlegen des ausführbaren Texts des Befehls (z. B. eine SQL-Anweisung) mit der [CommandText](commandtext-property-ado.md)-Eigenschaft.

  - Festlegen von parametrisierten Abfragen oder von Argumenten für gespeicherte Prozeduren mit [Parameter](parameter-object-ado.md)-Objekten und der [Parameters](parameters-collection-ado.md)-Auflistung.

  - Ausführen eines Befehls und Rückgabe eines **Recordset** -Objekts, falls zutreffend, mit der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode.

  - Festlegen des Befehlstyps mit der [CommandType](commandtype-property-ado.md)-Eigenschaft vor dem Ausführen des Befehls, um die Leistung zu optimieren.

  - Steuern, ob der Anbieter vor dem Ausführen eine vorbereitete (oder kompilierte) Version des Befehls speichert, mit der [Prepared](prepared-property-ado.md)-Eigenschaft.

  - Festlegen, wie viele Sekunden ein Anbieter auf die Ausführung eines Befehls wartet, mithilfe der [CommandTimeout](commandtimeout-property-ado.md)-Eigenschaft.

  - Zuordnen einer geöffneten Verbindung zu einem **Command** -Objekt, indem dessen [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt wird.

  - Festlegen der [Name](name-property-ado.md) -Eigenschaft, um das **Command** -Objekt als Methode im zugeordneten [Connection](connection-object-ado.md) -Objekt zu identifizieren.

  - Übergeben eines **Command** -Objekts an die [Source](source-property-ado-recordset.md)-Eigenschaft eines **Recordset** -Objekts, um Daten abzurufen.

  - Zugreifen auf anbieterspezifische Attribute für die [Properties](properties-collection-ado.md)-Auflistung.

> [!NOTE]
> [!HINWEIS] Sie können eine Abfrage ausführen, ohne ein **Command** -Objekt zu verwenden, indem Sie eine Abfragezeichenfolge an die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-Methode eines **Connection** -Objekts oder an die [Open](open-method-ado-recordset.md)-Methode eines **Recordset** -Objekts übergeben. Es ist jedoch ein **Command** -Objekt erforderlich, wenn der Befehlstext gespeichert und erneut ausgeführt werden soll. Sie können aber auch Abfrageparameter verwenden.

Wenn Sie ein **Command** -Objekt unabhängig von einem zuvor definierten **Connection** -Objekt erstellen möchten, geben Sie für seine **ActiveConnection** -Eigenschaft eine gültige Verbindungszeichenfolge an. ADO erstellt auch in diesem Fall ein **Connection** -Objekt, weist das Objekt aber keiner Objektvariablen zu. Wenn Sie jedoch derselben Verbindung mehrere **Command** -Objekte zuordnen, müssen Sie ein **Connection** -Objekt explizit erstellen und öffnen. Auf diese Weise wird dem **Connection** -Objekt eine Objektvariable zugeordnet. Wenn Sie die **ActiveConnection** -Eigenschaft des **Command** -Objekts nicht auf diese Objektvariable festlegen, erstellt ADO für jedes **Command** -Objekt ein neues **Connection** -Objekt, selbst wenn Sie dieselbe Verbindungszeichenfolge verwenden.

Sie führen ein **Command** -Objekt aus, indem Sie es einfach mit seiner [Name](name-property-ado.md)-Eigenschaft im zugeordneten **Connection** -Objekt aufrufen. Die **ActiveConnection** -Eigenschaft des **Command** -Objekts muss den Wert des **Connection** -Objekts haben. Wenn das **Command** -Objekt Parameter besitzt, übergeben Sie diese als Argumente an die Methode.

Wenn zwei oder mehrere **Command** -Objekte auf derselben Verbindung ausgeführt werden und eines der beiden **Command** - Objekte eine gespeicherte Prozedur ohne Parameter ist, tritt ein Fehler auf. Verwenden Sie unterschiedliche Verbindungen, oder trennen Sie alle anderen **Command** -Objekte von der Verbindung, um alle **Command** -Objekte auszuführen.

Die **Parameters** -Auflistung ist das Standardmitglied des **Command** -Objekts. Daher haben die beiden folgenden Codeanweisungen dieselbe Bedeutung.

