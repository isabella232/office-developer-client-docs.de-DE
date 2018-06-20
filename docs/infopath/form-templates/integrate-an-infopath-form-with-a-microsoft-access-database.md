---
title: Integrieren eines InfoPath-Formulars in eine Microsoft Access-Datenbank
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: Microsoft InfoPath unterstützt die Verwendung einer Microsoft Access 2010-Datenbank als primäre Datenquelle für ein Formular oder als sekundäre Datenquelle für ein Formular oder Steuerelement. In diesem Artikel wird erläutert, wie Access 2010-Datenbank als Datenquelle verwendet wird.
ms.openlocfilehash: 30aea15a5e9a8d19f64b3f089b71e859cff93e0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790789"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>Integrieren eines InfoPath-Formulars in eine Microsoft Access-Datenbank

Microsoft InfoPath unterstützt die Verwendung einer Microsoft Access 2010-Datenbank als primäre Datenquelle für ein Formular oder als sekundäre Datenquelle für ein Formular oder Steuerelement. In diesem Artikel wird erläutert, wie Access 2010-Datenbank als Datenquelle verwendet wird.
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>Verwenden einer Microsoft Access-Datenbank als Datenquelle

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Einrichten einer Microsoft Access-Datenbank als primäre Datenquelle eines Formulars

Datenbankverbindungen werden in InfoPath mithilfe des **Datenverbindungs-Assistenten**festgelegt. Dieser Assistent wird geöffnet, indem **Datenbank** im Abschnitt **Erweiterte Formularvorlagen** auf der Registerkarte **neu** von der Microsoft Office Backstage auswählen, und dann auf **Dieses Formular entwerfen**drücken.
  
Durch Klicken auf **Datenbank auswählen**, können Sie eine vorhandene Datenquelle auswählen oder direkt an einer bestimmten Datenbankdatei herstellen.
  
Nachdem Sie eine Datenbank ausgewählt haben, fordert der Assistent zum Auswählen einer Tabelle aus der Datenbank als Datenquelle für das Formular verwenden. Beim Hinzufügen von Tabellen deren Beziehung zueinander eingerichtet sind, und der Assistent zeigt die Tabellen und ihre hierarchischen Beziehungen in der Liste **Datenquellen-Struktur** . Wenn Sie das Kontrollkästchen **Tabellenspalten anzeigen** auswählen, zeigt der Assistent die Feldnamen jeder Tabelle in der Liste Datenquelle Struktur; Verwenden Sie die Kontrollkästchen neben den einzelnen Feldnamen an, ob ein Feld in der SQL-Anweisung enthalten ist, die vom Assistenten erstellten. 
  
> [!NOTE]
> Primäre Schlüsselfelder aus den einzelnen Tabellen sind immer ausgewählt und können nicht entfernt werden. 
  
Wenn die Tabellen, Felder und Beziehungen mit dem **Datenverbindungs-Assistenten angegeben wurden**, können Sie durch Klicken auf **SQL bearbeiten** , um die SQL-Anweisung anzuzeigen, die zum Einrichten der Datenquelle für das Formular verwendet wird. Klicken Sie im Dialogfeld **SQL bearbeiten** können Sie die **SQL-Anweisung überprüfen** , um sicherzustellen, dass InfoPath die Datenquelle aus den bereitgestellten Informationen erstellt werden klicken. Sie können auch im Dialogfeld **SQL bearbeiten** zum Ändern der SQL-Anweisung zum Erstellen komplexer Abfragen verwenden. 
  
> [!NOTE]
> Bei den von InfoPath verwendeten SQL-Anweisungen handelt es sich um Datenstrukturierungsabfragen. Sie ermöglichen das Erstellen hierarchischer Beziehungen zwischen mindestens zwei logischen Entitäten in einer Abfrage. JOIN-SQL-Anweisungen können verwendet werden. Allerdings wird davon abgeraten, da dann keine Formulare gesendet werden können. Weitere Informationen zu Datenstrukturierungsabfragen finden Sie in der Dokumentation im Microsoft Developer Network (MSDN). 
  
Die letzte Seite des **Datenverbindungs-Assistenten** werden zusammenfassende Informationen zu der Datenquelle, einschließlich der Name und der Dateiname der Datenquelle, den Namen der primären übergeordneten Tabelle, die Anzahl der Tabellen verwendet, und der Sendestatus. Der Submit-Status erfahren Sie, ob die generierte SQL-Anweisung für die erfolgreiche Übermittlung von Daten an die Datenquelle zulässig. 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Einrichten einer Microsoft Access-Datenbank als sekundäre Datenquelle

Sekundäre Datenquellen können verwendet werden, um die Einträge zu einem Listenfeld oder Dropdown-Listenfeld bereitstellen, oder Sie können Code schreiben, um Daten aus einer sekundären Datenquelle zum Formular hinzufügen. Klicken Sie zum Arbeiten mit sekundären Datenquellen im Formular **Datenverbindungen** auf der Registerkarte **Daten** auf, beim Entwerfen eines Formulars. 
  
Wenn Sie den **Datenverbindungs-Assistenten**zu starten, werden Sie aufgefordert, ob Daten im Formular verwenden oder zum Senden von Daten im Formular angezeigt werden soll. Wählen Sie **Daten empfangen**, und klicken Sie dann auf **Weiter**. Um eine sekundäre Datenquelle aus einer Datenbank zu erstellen, wählen Sie **Datenbank (Microsoft SQL Server oder Microsoft Office Access)**. Klicken Sie auf der nächsten Seite des Assistenten auf **Datenbank auswählen** , um eine vorhandene Datenquelle auswählen oder direkt an einer bestimmten Datenbankdatei herstellen. 
  
Nachdem Sie eine Datenbank ausgewählt haben, fordert der Assistent zum Auswählen einer Tabelle oder Abfrage aus der Datenbank als Datenquelle für das Formular verwenden. Sie müssen wählen Sie eine Tabelle oder Abfrage als Ausgangspunkt, aber Sie können zusätzliche Tabellen weiter unten auswählen, wenn Sie einschließen möchten. Nachdem Sie eine Tabelle oder Abfrage ausgewählt haben, können der Assistenten die Felder aus, den, die Sie in der Liste **Datenquelle Struktur** verwenden möchten. Standardmäßig werden alle Felder der Tabelle ausgewählt, jedoch können Sie Felder entfernen, wenn sie nicht für Ihr Formular erforderlich sind. Sie können auch steuern, wie aus der Tabelle zurückgegebenen Datensätze sortiert werden und ob mehrere Datensätze zulässig sind. Hierzu klicken Sie auf die **Tabelle ändern**, und wählen Sie dann im Dialogfeld **Sortierreihenfolge** bis zu drei Sortierkriterien aus. Wenn Sie davon überzeugt sind, klicken Sie auf **Fertig stellen**.
  
> [!NOTE]
> Primäre Schlüsselfelder aus den einzelnen Tabellen sind immer ausgewählt und können nicht entfernt werden. 
  
InfoPath können Sie Daten aus mehreren Tabellen oder Abfragen gleichzeitig abrufen. Beim Abrufen von Daten aus mehreren Tabellen oder Abfragen, müssen Sie möglicherweise eine Beziehung zwischen allen der beteiligten Tabellen oder Abfragen mit der ursprünglichen Tabelle oder Abfrage, die Sie im **Datenverbindungs-Assistenten**ausgewählt herstellen. Wenn Sie Daten aus der Customers-Tabelle der Northwind-Datenbank abrufen wurden, konnten Sie die Orders-Tabelle zum Abrufen von Daten über alle Aufträge für diesen Kunden hinzufügen ein, und Sie könnten die Tabelle Bestelldetails rufen Sie die Details zur Bestellung hinzufügen.
  
Um eine zusätzliche Tabelle auf die Datenquelle hinzuzufügen, wählen Sie die Tabelle, die Sie in der Liste **Datenquelle Struktur** untergeordnete Tabelle hinzufügen möchten, und klicken Sie dann auf **Tabelle hinzufügen**. Wählen Sie die Tabelle oder Abfrage, die Sie hinzufügen möchten, und klicken Sie dann auf **Weiter**. InfoPath aufgefordert, wählen Sie die Beziehung oder Beziehungen, den, die Sie verwenden möchten. Wenn Sie Felder in den beiden Tabellen, InfoPath automatisch gleichnamige fügt diese Felder als eine Beziehung nicht, oder wenn Sie eine benutzerdefinierte Beziehung verwenden möchten, klicken Sie auf **Beziehung hinzufügen** , um anzugeben, welche Felder in der übergeordneten Tabelle Feldern entsprechen in der untergeordneten Tabelle. Sie können auch vorhandene Beziehungen entfernen, indem Sie auf **Beziehung entfernen** im Dialogfeld **Beziehung bearbeiten** . 
  
Wenn Sie mit den Beziehungen zufrieden sind, klicken Sie auf **Fertig stellen**. Wie bei den wichtigsten Tabelle können Sie angeben, welche Felder aus der untergeordneten Tabelle zurückgegeben werden. Sie ist nicht möglich, jedoch die **Tabelle ändern** -Schaltfläche verwenden, um die Reihenfolge ändern, in der die Datensätze zurückgegeben werden. 
  
Wenn die Tabellen, Felder und Beziehungen angegeben haben, können Sie durch Klicken auf **SQL bearbeiten** , um die SQL-Anweisung der Abfrage anzeigen, die zum Einrichten der Datenquelle für das Formular verwendet wird. Klicken Sie im Dialogfeld **SQL bearbeiten** können Sie die **SQL-Anweisung überprüfen** , um sicherzustellen, dass InfoPath die Datenquelle aus den bereitgestellten Informationen erstellt werden klicken. Sie können auch im Dialogfeld **SQL bearbeiten** zum Ändern der SQL-Anweisung zum Erstellen komplexer Abfragen verwenden. 
  
> [!NOTE]
> Bei den von InfoPath verwendeten SQL-Anweisungen handelt es sich um Datenstrukturierungsabfragen. Sie ermöglichen das Erstellen hierarchischer Beziehungen zwischen mindestens zwei logischen Entitäten in einer Abfrage. JOIN-SQL-Anweisungen können verwendet werden. Allerdings wird davon abgeraten, da dann keine Formulare gesendet werden können. Weitere Informationen zu Datenstrukturierungsabfragen finden Sie in der Dokumentation im Microsoft Developer Network (MSDN). 
  
## <a name="enabling-form-submission"></a>Aktivieren des Sendens von Formularen

Zusätzlich zum Empfangen von Daten aus einer Access-Datenbank, kann InfoPath neue oder geänderte Daten zurück an die Datenbank übermitteln. Wenn Sie den Befehl **Absenden** auf der Registerkarte **Start** oder der Microsoft Office Backstage zum Übermitteln von Änderungen an der Datenbank verwenden, wird InfoPath ActiveX Data Objects (ADO) zum Aktualisieren der Datensätze in der Datenbank verwendet. Absenden des Formulars ist aktiviert, wenn alle der folgenden Bedingungen erfüllt sind: 
  
- Für jede in der Formularabfrage verwendete Spalte muss eine Basisspalte vorhanden sein.
    
- Eine Tabellenspalte darf in der gesamten Abfrage nicht mehrmals vorhanden sein.
    
- Ein Primärschlüssel, eine Eindeutigkeitseinschränkung oder ein eindeutiger Index muss für jede Tabelle in einer SELECT-Klausel vorhanden sein, die in der Formularabfrage verwendet wird.
    
- Eine Tabelle darf in der Formularabfrage nicht mehrmals vorhanden sein.
    
- Beziehungen zwischen über- und untergeordneten Tabellen müssen alle Primärschlüsselspalten aus der übergeordneten Tabelle enthalten.
    
- Für alle Spalten in einer SELECT-Klausel, die in der Formularabfrage verwendet wird, darf nur eine Basistabelle vorhanden sein.
    
Es gibt einige Situationen unter denen InfoPath Form Änderungen an eine Datenbank senden kann. Angenommen, wenn Sie ein Formular erstellen zeichnet, die Daten aus einer Abfrage anstelle einer Tabelle, oder wenn Sie die SQL-Anweisung, die von InfoPath anpassen Einbeziehung eine JOIN-Anweisung verwendet wird, wird InfoPath kann nicht zum Senden von Änderungen werden. Eine andere Umstand, der InfoPath Übermitteln von Änderungen verhindern würden ist, wenn Sie das Formular, das eine-n-Beziehung zu ihrer übergeordneten Tabelle Tabellen hinzugefügt wurden. In Situationen, in denen InfoPath kann nicht zum Senden von Änderungen an der Datenbank wird, wird das Feld **Submit-Status** auf der letzten Seite des **Datenverbindungs-Assistenten** den Grund für die Einschränkung angezeigt. 
  

