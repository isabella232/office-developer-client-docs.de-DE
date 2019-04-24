---
title: Recordset. CacheStart-Eigenschaft (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300616"
---
# <a name="recordsetcachestart-property-dao"></a>Recordset. CacheStart-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CacheStart

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie Daten von einem Remoteserver mit **Recordset**-Objekten abrufen, kann die Leistung durch eine Zwischenspeicherung gesteigert werden. Ein Zwischenspeicher ist ein Bereich im lokalen Speicher, an dem die zuletzt vom Server abgerufenen Daten gespeichert werden. Dies ist nützlich, wenn Benutzer dieselben Daten während der Ausführung des Programms wiederholt abrufen. Wenn Benutzer Daten abrufen, überprüft die Microsoft Access-Datenbank-Engine, ob die Daten im Zwischenspeicher enthalten sind, anstatt sie vom Server abzurufen. Dies erfordert weniger Zeit. Im Zwischenspeicher werden nur Daten gespeichert, die aus einer ODBC-Datenquelle stammen.

Jede ODBC-Datenquelle, die mit einer Microsoft Access-Datenbank-Engine verknüpft ist, wie etwa eine verknüpfte Tabelle, kann einen lokalen Zwischenspeicher haben. Zum Erstellen des Zwischenspeichers öffnen Sie ein **Recordset**-Objekt in der Remotedatenquelle und legen die Eigenschaften **CacheSize** und **[CacheStart](recordset-cachestart-property-dao.md)** fest. Anschließend verwenden Sie die **[FillCache](recordset-fillcache-method-dao.md)** -Methode oder durchlaufen die Datensätze mit den **Move**-Methoden.

Der Wert der **CacheStart**-Eigenschaft ist das Lesezeichen des ersten Datensatzes im **Recordset**-Objekt, das zwischengespeichert werden soll. Sie können das Lesezeichen jedes beliebigen Datensatzes verwenden, um die **CacheStart**-Eigenschaft festzulegen. Machen Sie den Datensatz, bei dem der Zwischenspeicher starten soll, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den Wert der **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft fest.

Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.

Aus dem Zwischenspeicher abgerufene Datensätze spiegeln die Änderungen, die gleichzeitig von anderen Benutzern vorgenommen wurden, nicht wider.

Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.

