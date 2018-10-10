---
title: Recordset2.CacheStart Property (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c44d70323976ade2017d406b628d3347b414f6aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475333"
---
# <a name="recordset2cachestart-property-dao"></a>Recordset2.CacheStart Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CacheStart

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Das Zwischenspeichern von Daten erhöht die Leistung, wenn Sie **Recordset**-Objekte zum Abrufen von Daten eines Remoteservers verwenden. Ein Cache ist ein Bereich im lokalen Arbeitsspeicher, in dem die zuletzt vom Server abgerufenen Daten aufbewahrt werden. Das ist praktisch, wenn die Daten während der Ausführung der Anwendung erneut vom Benutzer abgerufen werden. Fordern Benutzer Daten an, sucht das Microsoft Access-Datenbankmodul zuerst im Cache nach den angeforderten Daten, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur von ODBC-Datenquellen stammende Daten gespeichert.

Jede mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle (wie z. B. eine verknüpfte Tabelle) kann einen lokalen Cache besitzen. Öffnen Sie zum Erstellen eines Caches ein **Recordset**-Objekt in der Remotedatenquelle, legen Sie die Eigenschaften **CacheSize** und **[CacheStart](recordset2-cachestart-property-dao.md)** fest, und verwenden Sie dann die **[FillCache](recordset2-fillcache-method-dao.md)** -Methode, oder wechseln Sie mit den **Move**-Methoden durch die Datensätze.

Die Einstellung der **CacheStart**-Eigenschaft ist die Textmarke des ersten Datensatzes im zwischenzuspeichernden **Recordset**-Objekt. Sie können die Textmarke jedes beliebigen Datensatzes zum Festlegen der **CacheStart**-Eigenschaft verwenden. Machen Sie den Datensatz, mit dem Sie den Cache beginnen möchten, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den gleichen Wert wie die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft fest.

Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.

Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.

