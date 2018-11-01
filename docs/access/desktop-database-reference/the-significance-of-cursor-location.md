---
title: Bedeutung der Cursorplatzierung
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 092e14f314b4bba1e49cbb4ad7707aad0311bfbc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880446"
---
# <a name="the-significance-of-cursor-location"></a>Bedeutung der Cursorplatzierung


**Betrifft**: Access 2013, Office 2013

Jeder Cursor verwendet temporäre Ressourcen zum Speichern der Daten. Bei diesen Ressourcen kann es sich um Arbeitsspeicher, eine Auslagerungsdatei auf einer Festplatte, temporäre Dateien auf der Festplatte oder sogar temporären Speicherplatz in der Datenbank handeln. Der Mauszeiger wird einen *clientseitige* Cursor aufgerufen, wenn diese Ressourcen auf dem Clientcomputer gespeichert sind. Der Cursor ist einen *serverseitige* Cursor bezeichnet, wenn diese Ressourcen auf dem Server gespeichert sind.

## <a name="client-side-cursors"></a>Clientseitige Cursor

In ADO rufen Sie einen clientseitigen Cursor mithilfe der **adUseClient** -Eigenschaft von **CursorLocationEnum** auf. Bei einem clientseitigen Nicht-Keysetcursor sendet der Server das gesamte Resultset über das Netzwerk an den Clientcomputer. Der Clientcomputer stellt die temporären Ressourcen, die vom Cursor und vom Resultset benötigt werden, bereit und verwaltet sie. Die clientseitige Anwendung kann das gesamte Resultset durchsuchen, um die benötigten Zeilen zu bestimmen.

Statische und keysetgesteuerte clientseitige Cursor können eine erhebliche Last für die Arbeitsstation bedeuten, falls sie zu viele Zeilen enthalten. Alle Cursorbibliotheken können zwar Cursor mit Tausenden von Zeilen erstellen, aber Anwendungen zum Abrufen solch umfangreicher Rowsets weisen möglicherweise eine beeinträchtigte Leistung auf. Es gibt natürlich Ausnahmen. Für manche Anwendungen kann ein umfangreicher clientseitiger Cursor perfekt geeignet sein und die Leistung stellt kein Problem dar.

Ein offensichtlicher Vorteil des clientseitigen Cursors ist die schnelle Reaktion. Nachdem das Resultset auf den Clientcomputer heruntergeladen wurde, werden die Zeilen sehr schnell durchsucht. Die Anwendung ist bei clientseitigen Cursorn im Allgemeinen skalierbarer, weil die Ressourcenanforderungen des Cursors auf jeden einzelnen Client und nicht auf den Server verteilt werden.

## <a name="server-side-cursors"></a>Serverseitige Cursor

In ADO rufen Sie einen serverseitigen Cursor mithilfe der **adUseServer** -Eigenschaft von **CursorLocationEnum** auf. Bei einem serverseitigen Cursor verwaltet der Server das Resultset mithilfe von Ressourcen, die vom Servercomputer bereitgestellt werden. Der serverseitige Cursor gibt nur die angeforderten Daten über das Netzwerk zurück. Diese Art von Cursor bietet manchmal eine bessere Leistung als der clientseitige Cursor, insbesondere in Situationen, in denen übermäßiger Netzwerkverkehr ein Problem darstellt.

Es muss jedoch unbedingt darauf hingewiesen werden, dass ein serverseitiger Cursor - zumindest vorübergehend - für jeden aktiven Client wertvolle Serverressourcen belegt. Sie müssen entsprechend planen, um sicherzustellen, dass die Serverhardware alle von aktiven Clients angeforderten serverseitigen Cursor verwalten kann. Außerdem kann ein serverseitiger Cursor langsam sein, weil er nur den Zugriff auf einzelne Zeilen ermöglicht. Es ist nämlich kein Batchcursor verfügbar.

Serverseitige Cursor sind hilfreich beim Einfügen, Aktualisieren oder Löschen von Datensätzen. Bei serverseitigen Cursorn sind für eine Verbindung mehrere aktive Anweisungen möglich.

