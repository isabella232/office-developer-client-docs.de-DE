---
title: Sicherstellen von ausreichend Speicherplatz für TempDB
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09671570865d25738b7d4ba9358754c62da6f24e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946349"
---
# <a name="ensuring-sufficient-tempdb-space"></a>Sicherstellen von ausreichend Speicherplatz für TempDB


**Betrifft**: Access 2013, Office 2013

Falls bei der Bearbeitung von [Recordset](recordset-object-ado.md)-Objekten, die Verarbeitungskapazitäten von Microsoft SQL Server 6.5 benötigen, Fehler auftreten, müssen Sie möglicherweise TempDB vergrößern. (Einige Abfragen erfordern temporäre Verarbeitungskapazitäten. Eine Abfrage mit einer ORDER BY-Klausel erfordert z. B. eine Sortierung des **Recordset** -Objekts, was temporären Speicherplatz in Anspruch nimmt.)

> [!IMPORTANT]
> [!WICHTIG] Lesen Sie dieses Verfahren zuerst durch, bevor Sie die Aktionen ausführen, da ein Medium schwer wieder zu verkleinern ist, nachdem es vergrößert wurde.

> [!NOTE]
> [!HINWEIS] In Microsoft SQL Server 7.0 oder höher ist TempDB standardmäßig so eingerichtet, dass eine automatische Vergrößerung stattfindet. Dieses Verfahren ist deshalb möglicherweise nur bei Servern erforderlich, auf denen niedrigere Versionen als 7.0 ausgeführt werden.



**So vergrößern Sie den Speicherplatz von TempDB in SQL Server 6.5**

1.  Starten Sie Microsoft SQL Server Enterprise Manager, öffnen Sie die Struktur für den Server, und öffnen Sie dann die Struktur Datenbankmedien.

2.  Wählen Sie ein (physisches) Medium zum Vergrößern aus, z. B. Master, und doppelklicken Sie auf das Medium, um das Dialogfeld **Datenbankmedium bearbeiten** zu öffnen. Dieses Dialogfeld zeigt, wie viel Speicherplatz die aktuellen Datenbanken belegen.

3.  Erweitern Sie im Feld **Größe** das Medium auf die gewünschte Größe (z. B. 50 MB Festplattenspeicher).

4.  Klicken Sie auf **Jetzt ändern**, um den Speicherplatz zu vergrößern, den die (logische) TempDB maximal belegen kann.

5.  Erweitern Sie die Struktur der Datenbanken auf dem Server, und doppelklicken Sie auf **TempDB**, um das Dialogfeld **Datenbank bearbeiten** zu öffnen. Auf der Registerkarte **Datenbank** wird der Speicherplatz aufgeführt, der aktuell für TempDB reserviert ist (**Datengröße**). Standardmäßig sind das 2 MB.

6.  Klicken Sie in der Gruppe **Größe** auf **Vergrößern**. Das Diagramm zeigt den verfügbaren und den reservierten Speicherplatz aller physischen Medien an. Die braunen Balken stellen den verfügbaren Speicherplatz dar.

7.  Wählen Sie ein Protokollmedium aus, z. B. **Master**, um den verfügbaren Speicherplatz im Feld **Größe (MB)** anzuzeigen.

8.  Klicken Sie auf **Jetzt erweitern**, um diesen Speicherplatz für die TempDB-Datenbank zu reservieren. Das Dialogfeld **Datenbank bearbeiten** zeigt die neu reservierte Größe für TempDB an.

Weitere Informationen zu diesem Thema finden Sie in der Hilfe zu Microsoft SQL Server Enterprise Manager unter Datenbank vergrößern (Dialogfeld).

