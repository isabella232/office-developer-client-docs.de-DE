---
title: Integrieren eines InfoPath-Formulars in eine Microsoft Access-Datenbank
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: Microsoft InfoPath unterstützt die Verwendung einer Microsoft Access 2010-Datenbank als primäre Datenquelle für ein Formular oder als sekundäre Datenquelle für ein Formular oder Steuerelement. In diesem Artikel wird erläutert, wie Sie eine Access 2010-Datenbank als Datenquelle verwenden.
ms.openlocfilehash: dbc39e0d0908214904d77b8955f3d231f0bfb20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303514"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>Integrieren eines InfoPath-Formulars in eine Microsoft Access-Datenbank

Microsoft InfoPath unterstützt die Verwendung einer Microsoft Access 2010-Datenbank als primäre Datenquelle für ein Formular oder als sekundäre Datenquelle für ein Formular oder Steuerelement. In diesem Artikel wird erläutert, wie Sie eine Access 2010-Datenbank als Datenquelle verwenden.
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>Verwenden einer Microsoft Access-Datenbank als Datenquelle

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Einrichten einer Microsoft Access-Datenbank als primäre Datenquelle eines Formulars

Datenbankverbindungen werden in InfoPath mithilfe des datenVerbindungs- **Assistenten**eingerichtet. Dieser Assistent wird geöffnet, indem Sie im Abschnitt **Erweiterte Formularvorlagen** auf der Registerkarte **neu** in Microsoft Office backstaging die Option **Datenbank** auswählen und dann auf **dieses Formular entwerfen**klicken.
  
Durch Klicken auf **Datenbank auswählen** können Sie eine vorhandene Datenquelle auswählen oder eine direkte Verbindung mit einer bestimmten Datenbankdatei herstellen.
  
Nach der Auswahl einer Datenbank werden Sie vom Assistenten aufgefordert, in der Datenbank eine Tabelle auszuwählen, die als Datenquelle für das Formular verwendet werden soll. Beim Hinzufügen von Tabellen werden deren Beziehungen untereinander eingerichtet, und vom Assistenten werden die Tabellen und deren hierarchische Beziehungen in der Liste **Datenquellenstruktur** angezeigt. Wenn Sie das Kontrollkästchen **Tabellenspalten anzeigen** aktivieren, werden die Feldnamen jeder Tabelle in der Liste mit den Datenquellenstrukturen angezeigt. Mithilfe der Kontrollkästchen neben den einzelnen Feldnamen geben Sie an, ob ein Feld in die vom Assistenten erstellte SQL-Anweisung eingeschlossen wird. 
  
> [!NOTE]
> Primäre Schlüsselfelder aus den einzelnen Tabellen sind immer ausgewählt und können nicht entfernt werden. 
  
Wenn die Tabellen, Beziehungen und Felder mit dem datenVerbindungs- **Assistenten**angegeben wurden, können Sie auf **SQL bearbeiten** klicken, um die SQL-Anweisung anzuzeigen, die zum Festlegen der Datenquelle für das Formular verwendet wird. Im Dialogfeld **SQL bearbeiten** können Sie auf **SQL-Anweisung überprüfen** klicken, um zu überprüfen, ob die Datenquelle von InfoPath anhand der eingegebenen Informationen erstellt werden kann. Außerdem können Sie mithilfe des Dialogfelds **SQL bearbeiten** die SQL-Anweisung ändern, um komplexere Abfragen zu erstellen. 
  
> [!NOTE]
> Bei den von InfoPath verwendeten SQL-Anweisungen handelt es sich um Datenstrukturierungsabfragen. Sie ermöglichen das Erstellen hierarchischer Beziehungen zwischen mindestens zwei logischen Entitäten in einer Abfrage. JOIN-SQL-Anweisungen können verwendet werden. Allerdings wird davon abgeraten, da dann keine Formulare gesendet werden können. Weitere Informationen zu Datenstrukturierungsabfragen finden Sie in der Dokumentation im Microsoft Developer Network (MSDN). 
  
Auf der letzten Seite im Datenverbindungs-Assistenten wird eine Zusammenfassung der Datenquelle angezeigt. Hierzu zählen der Name und der Dateispeicherort der Datenquelle, der Name der primären übergeordneten Tabelle, die Anzahl verwendeter Tabellen sowie der Sendestatus. Der Sendestatus zeigt an, ob die generierte SQL-Anweisung das erfolgreiche Senden der Daten an die Datenquelle ermöglicht. 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Einrichten einer Microsoft Access-Datenbank als sekundäre Datenquelle

Mithilfe sekundärer Datenquellen können die Einträge für ein Listenfeld oder ein Dropdown-Listenfeld bereitgestellt werden. Sie können aber auch Code schreiben, um Ihren Formularen Daten aus einer sekundären Datenquelle hinzuzufügen. Um sekundäre Datenquellen in Ihrem Formular zu verwenden, klicken Sie beim Entwerfen eines Formulars auf der Registerkarte **Daten** auf **Datenverbindungen**. 
  
Beim Starten des datenVerbindungs- **Assistenten**werden Sie aufgefordert auszuwählen, ob Daten im Formular empfangen oder Daten im Formular übermittelt werden sollen. Wählen Sie **Daten empfangen**aus, und klicken Sie dann auf **weiter**. Wenn Sie eine sekundäre Datenquelle aus einer Datenbank erstellen möchten, wählen Sie **Datenbank (nur Microsoft SQL Server oder Microsoft Office Access)** aus. Klicken Sie auf der nächsten Seite des Assistenten auf **Datenbank auswählen** , um eine vorhandene Datenquelle auszuwählen oder eine direkte Verbindung mit einer bestimmten Datenbankdatei herzustellen. 
  
	Nach der Auswahl einer Datenbank werden Sie vom Assistenten aufgefordert, in der Datenbank eine Tabelle oder Abfrage auszuwählen, die als Datenquelle für das Formular verwendet werden soll. Sie müssen zunächst eine Tabelle oder Abfrage auswählen, können aber später bei Bedarf weitere Tabellen auswählen. Nachdem Sie eine Tabelle oder Abfrage ausgewählt haben, können Sie die Felder auswählen, die Sie in der Liste **Datenquellenstruktur** verwenden möchten. Standardmäßig sind alle Felder der Tabelle ausgewählt. Sie können jedoch Felder entfernen, falls diese für Ihr Formular nicht erforderlich sind. Darüber hinaus können Sie die Sortierung der von der Tabelle zurückgegebenen Datensätze festlegen und angeben, ob mehrere Datensätze zulässig sind. Dazu klicken Sie auf **Tabelle ändern** und wählen dann im Dialogfeld **Sortierreihenfolge** bis zu drei Sortierkriterien aus. Klicken Sie auf **Fertig stellen**, wenn die Angaben Ihren Vorstellungen entsprechen.
  
> [!NOTE]
> Primäre Schlüsselfelder aus den einzelnen Tabellen sind immer ausgewählt und können nicht entfernt werden. 
  
In InfoPath können Sie auch Daten aus mehreren Tabellen oder Abfragen gleichzeitig abrufen. Wenn Sie Daten aus mehreren Tabellen oder Abfragen abrufen, müssen Sie in der Lage sein, eine Beziehung zwischen allen Tabellen oder Abfragen einzurichten, die mit der ursprünglichen Tabelle oder Abfrage verbunden sind, die Sie im datenVerbindungs- **Assistenten**ausgewählt haben. Wenn Sie beispielsweise Daten aus der Tabelle Customers der Northwind-Datenbank abgerufen haben, können Sie die Tabelle Orders hinzufügen, um Daten zu allen Bestellungen für diesen Kunden abzurufen, und Sie können die Tabelle Order Details hinzufügen, um die Details der einzelnen Reihenfolge abzurufen.
  
Um der Datenquelle eine zusätzliche Tabelle hinzuzufügen, wählen Sie in der Liste **Datenquellenstruktur** die Tabelle aus, der Sie eine untergeordnete Tabelle hinzufügen möchten, und klicken Sie dann auf **Tabelle hinzufügen**. Wählen Sie die Tabelle oder Abfrage aus, die Sie hinzufügen möchten, und klicken Sie dann auf **Weiter**. Sie werden von InfoPath aufgefordert, die gewünschte Beziehung bzw. die gewünschten Beziehungen auszuwählen. Falls Felder in den beiden Tabellen den gleichen Namen aufweisen, werden diese Felder von InfoPath automatisch als Beziehung hinzugefügt. Andernfalls, oder falls Sie eine benutzerdefinierte Beziehung verwenden möchten, können Sie auf **Beziehung hinzufügen** klicken, um anzugeben, welche Felder in der übergeordneten Tabelle Feldern in der untergeordneten Tabelle entsprechen. Außerdem können Sie vorhandene Beziehungen entfernen, indem Sie im Dialogfeld **Beziehung bearbeiten** auf **Beziehung entfernen** klicken. 
  
Klicken Sie auf **Fertig stellen**, wenn die Beziehungen Ihren Vorstellungen entsprechen. Wie bei der Haupttabelle können Sie angeben, welche Felder von der untergeordneten Tabelle zurückgegeben werden. Allerdings können Sie nicht mit der Schaltfläche **Tabelle ändern** die Reihenfolge bearbeiten, in der die Datensätze zurückgegeben werden. 
  
Nachdem die Tabellen, Beziehungen und Felder angegeben wurden, können Sie durch Klicken auf **SQL bearbeiten** die SQL-Abfrageanweisung anzeigen, mit der die Datenquelle für das Formular eingerichtet wird. Im Dialogfeld **SQL bearbeiten** können Sie auf **SQL-Anweisung überprüfen** klicken, um zu überprüfen, ob die Datenquelle von InfoPath anhand der eingegebenen Informationen erstellt werden kann. Außerdem können Sie mithilfe des Dialogfelds **SQL bearbeiten** die SQL-Anweisung ändern, um komplexere Abfragen zu erstellen. 
  
> [!NOTE]
> Bei den von InfoPath verwendeten SQL-Anweisungen handelt es sich um Datenstrukturierungsabfragen. Sie ermöglichen das Erstellen hierarchischer Beziehungen zwischen mindestens zwei logischen Entitäten in einer Abfrage. JOIN-SQL-Anweisungen können verwendet werden. Allerdings wird davon abgeraten, da dann keine Formulare gesendet werden können. Weitere Informationen zu Datenstrukturierungsabfragen finden Sie in der Dokumentation im Microsoft Developer Network (MSDN). 
  
## <a name="enabling-form-submission"></a>Aktivieren des Sendens von Formularen

Neben dem Empfangen von Daten von einer Access-Datenbank kann InfoPath neue oder geänderte Daten an die Datenbank zurücksenden. Wenn Sie auf der **** Registerkarte **Start** oder in Microsoft Office backstaging die Änderungen an der Datenbank übermitteln, verwendet InfoPath ActiveX Data Objects (ADO), um die Datensätze in der Datenbank zu aktualisieren. Das Senden von Formularen ist möglich, wenn alle folgenden Bedingungen erfüllt sind: 
  
- Für jede in der Formularabfrage verwendete Spalte muss eine Basisspalte vorhanden sein.
    
- Eine Tabellenspalte darf in der gesamten Abfrage nicht mehrmals vorhanden sein.
    
- Ein Primärschlüssel, eine Eindeutigkeitseinschränkung oder ein eindeutiger Index muss für jede Tabelle in einer SELECT-Klausel vorhanden sein, die in der Formularabfrage verwendet wird.
    
- Eine Tabelle darf in der Formularabfrage nicht mehrmals vorhanden sein.
    
- Beziehungen zwischen über- und untergeordneten Tabellen müssen alle Primärschlüsselspalten aus der übergeordneten Tabelle enthalten.
    
- Für alle Spalten in einer SELECT-Klausel, die in der Formularabfrage verwendet wird, darf nur eine Basistabelle vorhanden sein.
    
Es gibt einige Umstände, unter denen InfoPath keine Formular Änderungen an eine Datenbank übermitteln kann. Wenn Sie beispielsweise ein Formular erstellen, das Daten aus einer Abfrage anstelle einer Tabelle zeichnet, oder wenn Sie die SQL-Anweisung anpassen, die von InfoPath verwendet wird, um eine JOIN-Anweisung einzufügen, kann InfoPath keine Änderungen übermitteln. Wenn Sie dem Formulartabellen hinzufügen möchten, die eine viele-zu-eins-Beziehung mit der übergeordneten Tabelle aufweisen, können Sie verhindern, dass InfoPath Änderungen übermittelt. In Situationen, in denen InfoPath keine Änderungen an der Datenbank übermitteln kann, wird im Feld **Sendestatus** auf der letzten Seite des Datenverbindungs- **Assistenten** der Grund für die Einschränkung angezeigt. 
  

