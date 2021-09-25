---
title: Stream-Objekt (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6357a0f8ce0544294c54345bd5200b10b3fc95c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580755"
---
# <a name="stream-object-ado"></a>Stream-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Stellt einen Datenstrom von Binärdaten oder Text dar.

## <a name="remarks"></a>HinwBemerkungeneise

In strukturstrukturierten Hierarchien wie z. B. einem Dateisystem oder einem E-Mail-System ist einem [Datensatz](record-object-ado.md) möglicherweise ein standardmäßiger binärer Bitdatenstrom zugeordnet, der den Inhalt der Datei oder der E-Mail enthält. Mit einem **Stream** -Objekt können Felder oder Datensätze bearbeitet werden, die diese Datenströme enthalten. Sie können ein **Stream** -Objekt auf folgende Weise erhalten:

  - Von einer URL, die auf ein Objekt (gewöhnlich eine Datei) zeigt, das die Binär- oder Textdaten enthält. Dieses Objekt kann ein einfaches Dokument, ein **Record** -Objekt, das ein strukturiertes Objekt darstellt, oder ein Ordner sein.

  - Durch Öffnen des **Stream** -Objekts, das einem **Record** -Objekt zugeordnet ist. Sie erhalten den Standarddatenstrom, der einem **Record** -Objekt zugeordnet ist, wenn das **Record** -Objekt geöffnet wird, um einen Roundtrip zum Öffnen des Datenstroms zu vermeiden.

  - Durch Instanziieren eines **Stream** -Objekts. Dieses **Stream** -Objekt kann verwendet werden, um Daten für die Zwecke der Anwendung zu speichern. Im Unterschied zu einem **Stream** -Objekt, das einer URL zugeordnet ist, oder dem Standard- **Stream** -Objekt eines **Record** -Objekts ist ein instanziiertes **Stream** -Objekt keiner zugrunde liegenden Quelle standardmäßig zugeordnet.

Mit den Methoden und Eigenschaften eines **Stream** -Objekts können Sie die folgenden Aufgaben ausführen:

  - Öffnen eines **Stream** -Objekts eines **Record** -Objekts oder URLs mit der [Open](open-method-ado-stream.md)-Methode.

  - Schließen eines **Stream** -Objekts mit der [Close](close-method-ado.md)-Methode.

  - Eingeben von Bytes oder Text in ein **Stream** -Objekt mit den Methoden [Write](write-method-ado.md) und [WriteText](writetext-method-ado.md).

  - Lesen von Bytes vom **Stream** -Objekt mit den Methoden [Read](read-method-ado.md) und [ReadText](readtext-method-ado.md).

  - Schreiben beliebiger **Stream** -Daten, die noch im ADO-Puffer sind, in das zugrunde liegende Objekt mit der [Flush](flush-method-ado.md)-Methode.

  - Kopieren des Inhalts eines **Stream** -Objekts in ein anderes **Stream** -Objekt mit der [CopyTo](copyto-method-ado.md)-Methode.

  - Steuern, wie Zeilen aus der Quelldatei gelesen werden, mit der [SkipLine](skipline-method-ado.md)-Methode und der [LineSeparator](lineseparator-property-ado.md)-Eigenschaft.

  - Festlegen der Position des Datenstromendes mit der [EOS](eos-property-ado.md)-Eigenschaft und der [SetEOS](seteos-method-ado.md)-Methode.

  - Speichern und Wiederherstellen von Daten in Dateien mit den Methoden [SaveToFile](savetofile-method-ado.md) und [LoadFromFile](loadfromfile-method-ado.md).

  - Bestimmen des Zeichensatzes, der zum Speichern des **Stream** -Objekts verwendet wird, mit der [Charset](charset-property-ado.md)-Eigenschaft.

  - Anhalten eines asynchronen **Stream** -Vorgangs mit der [Cancel](cancel-method-ado.md)-Methode.

  - Festlegen der Anzahl von Bytes in einem **Stream** -Objekt mit der [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream)-Eigenschaft.

  - Steuern der aktuellen Position innerhalb eines **Stream** -Objekts mit der [Position](position-property-ado.md)-Eigenschaft.

  - Bestimmen des Typs der Daten in einem **Stream** -Objekt mit der [Type](type-property-ado-stream.md)-Eigenschaft.

  - Bestimmen des aktuellen Zustands des **Stream** -Objekts (geschlossen, offen oder in Ausführung) mit der [State](state-property-ado.md)-Eigenschaft.

  - Festlegen des Zugriffsmodus für das **Stream** -Objekt mit der [Mode](mode-property-ado.md)-Eigenschaft.

> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


