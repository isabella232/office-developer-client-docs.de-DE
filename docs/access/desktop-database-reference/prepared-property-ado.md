---
title: Prepared-Eigenschaft (ADO)
TOCTitle: Prepared Property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865453f89cd5942ec7f9f8d036beb72dc519397e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472931"
---
# <a name="prepared-property-ado"></a>Prepared-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob eine kompilierte Version eines Befehls vor dem Ausführen gespeichert werden soll.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Boolean** -Wert fest oder gibt den Wert zurück. Ein Wert **True** gibt an, dass der Befehl vorbereitet werden soll.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Prepared** -Eigenschaft, wenn der Anbieter eine vorbereitete (bzw. kompilierte) Version der in der [CommandText](commandtext-property-ado.md)-Eigenschaft angegebenen Abfrage speichern soll, bevor ein [Command](command-object-ado.md)-Objekt erstmalig ausgeführt wird. Dadurch wird möglicherweise das erste Ausführen des zugehörigen Befehls zwar verlangsamt, aber da der Anbieter nach dem Kompilieren des Befehls die kompilierte Version zum weiteren Ausführen des Befehls verwendet, ergibt sich eine verbesserte Leistung.

Ist die Eigenschaft auf **False** festgelegt, führt der Anbieter das **Command** -Objekt direkt aus, ohne eine kompilierte Version zu erstellen.

Unterstützt der Anbieter die Vorbereitung von Befehlen nicht, wird möglicherweise ein Fehler zurückgegeben, sobald diese Eigenschaft auf **True** festgelegt wird. Wenn kein Fehler zurückgegeben wird, wird die Anforderung zum Vorbereiten des Befehls einfach ignoriert und die **Prepared** -Eigenschaft auf **False** festgelegt.

