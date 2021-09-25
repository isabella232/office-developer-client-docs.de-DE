---
title: Was ist ein Cursor?  (Access-Desktopdatenbankreferenz)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c8016f5deb22f5d5def560bfde9412624a3f6de7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572515"
---
# <a name="what-is-a-cursor"></a>Was ist ein Cursor?


**Gilt für**: Access 2013, Office 2013

Vorgänge in einer relationalen Datenbank fungieren auf einem vollständigen Zeilensatz. Der Zeilensatz, der von einer SELECT-Anweisung zurückgegeben wird, besteht aus allen Zeilen, die den Bedingungen in der WHERE-Klausel der Anweisung entsprechen. Dieser vollständige Zeilensatz, der von der Anweisung zurückgegeben wird, wird als Resultset bezeichnet. Anwendungen, insbesondere interaktive Anwendungen und Onlineanwendungen, können nicht immer effizient mit dem gesamten Resultset als eine Einheit arbeiten. Diese Anwendungen benötigen einen Mechanismus, um jeweils mit einer Zeile oder einem kleinen Zeilenblock zu arbeiten. Cursor sind eine Erweiterung für Resultsets, die diesen Mechanismus anbieten.

Ein Cursor wird von einer Cursorbibliothek implementiert. Eine Cursorbibliothek ist Software, die häufig als Teil eines Datenbanksystems oder einer Datenzugriffs-API implementiert wird und zum Verwalten der Attribute von Daten, die von einer Datenquelle (ein Resultset) zurückgegeben werden, verwendet wird. Zu diesen Attributen zählen Parallelitätsverwaltung, Position im Resultset, Anzahl der zurückgegebenen Zeilen sowie, ob die Navigation vorwärts und/oder rückwärts im Resultset möglich ist (Bildlauffähigkeit).

Ein Cursor verfolgt die Position im Resultset und ermöglicht die zeilenweise Ausführung mehrerer Vorgänge für ein Resultset, wobei zur ursprünglichen Tabelle zurückgekehrt wird, oder auch nicht. Cursor geben also ein Resultset basierend auf Tabellen innerhalb der Datenbanken zurück. Der Cursor heißt so, weil er die aktuelle Position im Resultset angibt, so wie der Cursor auf einem Computerbildschirm die aktuelle Position anzeigt.

Sie sollten sich unbedingt mit dem Cursorkonzept vertraut machen, bevor Sie sich mit den Einzelheiten ihrer Verwendung in ADO beschäftigen.

Cursor ermöglichen Folgendes:

  - Angeben der Position in bestimmten Zeilen im Resultset.

  - Abrufen einer Zeile oder eines Zeilenblocks basierend auf der aktuellen Resultsetposition.

  - Ändern von Daten in den Zeilen an der aktuellen Position im Resultset.

  - Definieren unterschiedlicher Ebenen der Empfindlichkeit gegenüber Datenänderungen durch andere Benutzer.

Angenommen, eine Anwendung zeigt einem potenziellen Käufer eine Liste verfügbarer Produkte an. Der Käufer führt einen Bildlauf in der Liste aus, um Produktdetails und Kosten anzuzeigen, und wählt schließlich ein Produkt für den Kauf aus. Für den Rest der Liste werden zusätzliche Bildlauf- und Auswahlschritte ausgeführt. Was den Käufer betrifft, werden die Produkte einzeln angezeigt, aber die Anwendung verwendet einen bildlauffähigen Cursor, um das Resultset nach oben und unten zu durchsuchen.

Sie können Cursor auf verschiedene Weise verwenden:

  - Ohne Zeilen.

  - Mit einigen oder allen Zeilen in einer einzelnen Tabelle.

  - Mit einigen oder allen Zeilen aus logisch verknüpften Tabellen.

  - Als schreibgeschützt oder aktualisierbar auf Cursor- oder Feldebene.

  - Als Vorwärtscursor oder voll bildlauffähigen Cursor.

  - Mit dem Cursorkeyset auf dem Server.

  - Empfindlich für Änderungen an zugrunde liegenden Tabellen durch andere Anwendungen (z. B. Mitgliedschaft, Sortierung, Einfügungen, Aktualisierungen und Löschvorgänge).

  - Auf dem Server oder auf dem Client vorhanden.

Mit schreibgeschützten Cursorn können Benutzer das Resultset durchsuchen, und Cursor mit Lese-/Schreibzugriff können einzelne Zeilenaktualisierungen implementieren. Komplexe Cursor können mit Keysets definiert werden, die auf Basistabellenzeilen zurückverweisen. Manche Cursor sind für die Vorwärtsnavigation schreibgeschützt, während andere Cursor rückwärts und vorwärts navigieren können und eine dynamische Aktualisierung des Resultsets basierend auf Änderungen durch andere Anwendungen an der Datenbank ermöglichen.

Nicht alle Anwendungen müssen Cursor verwenden, um auf Daten zuzugreifen oder diese zu aktualisieren. Manche Abfragen erfordern keine direkte Zeilenaktualisierung mithilfe eines Cursors. Cursor sollten eines der letzten Verfahren sein, die Sie zum Abrufen von Daten auswählen - und in diesem Fall sollten Sie den Cursor mit dem geringsten Aufwand auswählen. Wenn Sie ein Resultset mithilfe einer gespeicherten Prozedur erstellen, kann das Resultset nicht mit Cursorbearbeitungs- oder Cursoraktualisierungsmethoden aktualisiert werden.

## <a name="concurrency"></a>Parallelität

Bei manchen Mehrbenutzeranwendungen müssen die dem Endbenutzer angezeigten Daten unbedingt möglichst aktuell sein. Ein klassisches Beispiel für ein solches System ist ein Flugreservierungssystem, bei dem sich möglicherweise viele Benutzer um den gleichen Platz für einen bestimmten Flug schlagen (und damit einen einzelnen Datensatz). In diesem Fall muss der Anwendungsentwurf gleichzeitige Vorgänge für einen einzelnen Datensatz ermöglichen.

Bei anderen Anwendungen ist die Parallelität nicht so wichtig. In diesen Fällen ist der Aufwand, die Daten ständig auf dem aktuellen Stand zu halten, nicht gerechtfertigt.

## <a name="position"></a>Position

Ein Cursor verfolgt auch die aktuelle Position in einem Resultset. Stellen Sie sich die Cursorposition als Zeiger auf den aktuellen Datensatz vor, ähnlich wie ein Arrayindex auf den Wert an eben dieser Position im Array zeigt.

## <a name="scrollability"></a>Bildlauffähigkeit

Der von der Anwendung verwendete Cursortyp beeinflusst auch die Möglichkeit, in den Zeilen eines Resultsets vorwärts und rückwärts zu navigieren. Dies wird manchmal als Bildlauffähigkeit bezeichnet. Durch die Möglichkeit, in einem Resultset vorwärts *und* rückwärts zu navigieren, wird der Cursor komplexer und ist deshalb teurer in der Implementierung. Aus diesem Grund sollten Sie einen Cursor mit dieser Funktionalität nur im Bedarfsfall verwenden.

