---
title: Recordset.CacheStart-Eigenschaft (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699986"
---
# <a name="recordsetcachestart-property-dao"></a>Recordset.CacheStart-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CacheStart

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Das Zwischenspeichern von Daten erhöht die Leistung, wenn Sie **Recordset**-Objekte zum Abrufen von Daten eines Remoteservers verwenden. Ein Cache ist ein Bereich im lokalen Arbeitsspeicher, in dem die zuletzt vom Server abgerufenen Daten aufbewahrt werden. Das ist praktisch, wenn die Daten während der Ausführung der Anwendung erneut vom Benutzer abgerufen werden. Fordern Benutzer Daten an, sucht das Microsoft Access-Datenbankmodul zuerst im Cache nach den angeforderten Daten, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur von ODBC-Datenquellen stammende Daten gespeichert.

Jede mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle (wie z. B. eine verknüpfte Tabelle) kann einen lokalen Cache besitzen. Öffnen Sie zum Erstellen eines Caches ein **Recordset**-Objekt in der Remotedatenquelle, legen Sie die Eigenschaften **CacheSize** und **[CacheStart](recordset-cachestart-property-dao.md)** fest, und verwenden Sie dann die **[FillCache](recordset-fillcache-method-dao.md)** -Methode, oder wechseln Sie mit den **Move**-Methoden durch die Datensätze.

Die Einstellung der **CacheStart**-Eigenschaft ist die Textmarke des ersten Datensatzes im zwischenzuspeichernden **Recordset**-Objekt. Sie können die Textmarke jedes beliebigen Datensatzes zum Festlegen der **CacheStart**-Eigenschaft verwenden. Machen Sie den Datensatz, mit dem Sie den Cache beginnen möchten, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den gleichen Wert wie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft fest.

Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.

Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.

