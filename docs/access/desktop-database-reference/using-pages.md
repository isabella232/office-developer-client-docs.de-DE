---
title: Verwenden von Seiten (Access PC-Datenbank-Referenz)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b25123698f39e602b59a2f5cd6bd9a2f0595addb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475853"
---
# <a name="using-pages"></a>Verwenden von Seiten


**Betrifft**: Access 2013 | Office 2013

Mit der **PageCount** -Eigenschaft bestimmen Sie die Anzahl der Datenseiten im **Recordset** -Objekt. *Seiten* sind Datensatzgruppen, deren Größe der Einstellung der **PageSize** -Eigenschaft entspricht. Selbst wenn die letzte Seite unvollständig ist, weil weniger Datensätze vorhanden sind, als für die **PageSize** -Eigenschaft angegeben ist, zählt sie als zusätzliche Seite für **PageCount**. Wenn diese Eigenschaft vom **Recordset** -Objekt nicht unterstützt wird, hat **PageCount** den Wert -1, womit **PageCount** nicht bestimmt werden kann.

Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der **AbsolutePage** -Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist für Webserverszenarien hilfreich, wenn Sie dem Benutzer gestatten möchten, in den Daten zu blättern und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.

Diese Eigenschaft kann jederzeit festgelegt werden. Mit dem Wert dieser Eigenschaft wird die Position des ersten Datensatzes einer bestimmten Seite berechnet.

Mit der **AbsolutePage** -Eigenschaft identifizieren Sie die Nummer der Seite, auf der sich der aktuelle Datensatz befindet. Auch in diesem Fall muss die entsprechende Funktionalität vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

**AbsolutePage** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtanzahl der Seiten rufen Sie mit der **PageCount** -Eigenschaft ab.

