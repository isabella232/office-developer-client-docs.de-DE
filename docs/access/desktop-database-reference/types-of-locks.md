---
title: Typen von Sperren (Access PC-Datenbank-Referenz)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9aa0753892174995a8ffc0ee5901a86493f1349d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867510"
---
# <a name="types-of-locks"></a>Typen von Sperren


**Betrifft**: Access 2013, Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

Gibt optimistische Batchaktualisierungen an und ist für den Batchaktualisierungsmodus erforderlich.

Viele Anwendungen rufen eine Reihe von Zeilen gleichzeitig ab und müssen dann koordinierte Aktualisierungen vornehmen, die die gesamten Zeilen enthalten, die eingefügt, aktualisiert oder gelöscht werden sollen. Mit Batchcursorn ist nur ein Roundtrip zum Server erforderlich. Dadurch wird die Aktualisierungsleistung verbessert und der Netzwerkverkehr reduziert. Mit einer Batchcursorbibliothek können Sie einen statischen Cursor erstellen und dann die Verbindung mit der Datenquelle trennen. Nun können Sie die Zeilen ändern und anschließend erneut eine Verbindung herstellen und die Änderungen in einem Batch in der Datenquelle bereitstellen.

## <a name="adlockoptimistic"></a>adLockOptimistic

Gibt an, dass der Anbieter optimistische Sperren verwendet. Datensätze werden also nur gesperrt, wenn Sie die **Update** -Methode aufrufen. Es besteht deshalb die Möglichkeit, dass Daten zwischen Ihrer Bearbeitung des Datensatzes und dem Aufrufen von **Update** von einem anderen Benutzer geändert werden. Dadurch entstehen Konflikte. Verwenden Sie diesen Sperrtyp in Fällen, in denen die Chance von Konflikten niedrig ist oder in denen Konflikte auf einfache Weise gelöst werden können.

## <a name="adlockpessimistic"></a>adLockPessimistic

Gibt an, dass datensatzweise pessimistische Sperren verwendet werden. Der Anbieter unternimmt alles Erforderliche, um die erfolgreiche Bearbeitung der Datensätze sicherzustellen, indem er gewöhnlich Datensätze in der Datenquelle unmittelbar vor der Bearbeitung sperrt. Dies bedeutet natürlich, dass die Datensätze, sobald Sie mit dem Bearbeiten begonnen haben, erst wieder für andere Benutzer verfügbar sind, wenn Sie die Sperre durch Aufrufen von **Update** aufheben. Verwenden Sie diesen Sperrtyp für ein System, in dem gleichzeitige Änderungen an Daten auf keinen Fall zulässig sind, wie z. B. für ein Reservierungssystem.

## <a name="adlockreadonly"></a>adLockReadOnly

Gibt schreibgeschützte Datensätze an. Die Daten können nicht geändert werden. Eine schreibgeschützte Sperre ist der "schnellste" Sperrtyp, weil der Server keine Sperre in den Datensätzen verwalten muss.

## <a name="adlockunspecified"></a>adLockUnspecified

Gibt keinen Sperrtyp an.

