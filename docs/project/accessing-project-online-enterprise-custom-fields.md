---
title: Zugreifen auf benutzerdefinierte Project Online-Enterprise-Felder
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online ist ein Office 365-Dienst, den Unternehmen erweitern können, um Geschäftsanforderungen zu erfüllen. Ein Erweiterungsbereich sind benutzerdefinierte Enterprise-Felder (Enterprise Custom Fields, ECFs). ECFs sind typbehaftete Wertfelder, die Projekten, Ressourcen und Aufgaben hinzugefügt werden können. In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben verknüpft sind, und jeweils ein Beispiel eines Werts für eine Instanz des jeweiligen ECF aufgelistet:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708305"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Zugreifen auf benutzerdefinierte Project Online-Enterprise-Felder

Project Online ist ein Office 365-Dienst, den Unternehmen erweitern können, um Geschäftsanforderungen zu erfüllen. Ein Erweiterungsbereich sind benutzerdefinierte Enterprise-Felder (Enterprise Custom Fields, ECFs). ECFs sind typbehaftete Wertfelder, die Projekten, Ressourcen und Aufgaben hinzugefügt werden können. In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben verknüpft sind, und jeweils ein Beispiel eines Werts für eine Instanz des jeweiligen ECF aufgelistet:
  
|ECF-Name|ECF-Typ|Zuweisung|Beispielwert|
|:-----|:-----|:-----|:-----|
|Justification  <br/> |TEXT  <br/> |Project  <br/> |Ein Endbenutzer kann wichtige Statistiken und Zustandsdaten erfassen, mit Ergebnissen, die eine Zustandsbewertung und einen individualisierten Aktionsplan in Richtung Zustandsverbesserung beinhalten.  <br/> |
|Risikobewertung  <br/> |TEXT  <br/> |Project  <br/> |Niedrig  <br/> |
|ROI  <br/> |NUMBER  <br/> |Project  <br/> |2.10  <br/> |
|Total Cost  <br/> |COST  <br/> |Project  <br/> |$1.031.514  <br/> |
|Launch Team  <br/> |TEXT  <br/> |Ressourcen  <br/> |Ja  <br/> |
|Position Role  <br/> |TEXT  <br/> |Ressourcen  <br/> |Tester  <br/> |
|Flag Status  <br/> |FLAG  <br/> |Aufgabe  <br/> |No  <br/> |
|Health  <br/> |TEXT  <br/> |Aufgabe  <br/> |Nicht angegeben  <br/> |
   
ECFs sind in der Project Web Application-Instanz (PWA-Instanz) definiert, außerhalb von jedem Projekt, jeder Ressource oder jeder Aufgabe. Dennoch können sie mit einem Projekt, einer Ressource oder einer Aufgabe verknüpft werden. Dieser Artikel bietet eine einführende Sicht auf benutzerdefinierte Felder anhand einer Beispielanwendung und konzentriert sich auf das Abrufen von ECF-Werten. 
  
Sie können das vollständige Beispiel aus https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields herunterladen.
  
Darüber hinaus unterstützt Project Online lokale benutzerdefinierte Felder als schreibgeschützte Einheiten, die speziell für das jeweilige Objekt (Projekt, Ressource oder Aufgabe) gelten. Weitere Informationen zu lokalen benutzerdefinierten Feldern finden Sie im Beispiel https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Hintergrundmaterial

Ein vorheriger Artikel, [Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell](developing-a-project-online-application-using-the-client-side-object-model.md), bietet Hintergrundinformationen und die erste Orientierung für die Entwicklung von Anwendungen mit CSOM. In diesem Artikel finden Sie die folgenden Punkte:
  
- Hintergrundinformationen zu Project, eigenständige und cloudbasierte Editionen 
    
- Entwicklungsumgebung (Visual Studio-Editionen und Softwarebibliotheken)
    
- Einrichten eines Visual Studio-Projekts für eine .NET-Anwendung mit der CSOM-Bibliothek
    
- Herstellen einer Verbindung mit dem Project Online-Dienst
    
## <a name="preliminaries-class-level-declarations"></a>Vorbereitungen (Deklarationen auf Klassenebene)

Die Klasse für diese Anwendung definiert zwei Datenelemente: den Projektkontext und das pwaECF-Wörterbuch.
  
Das Projektkontextobjekt ist Bestandteil des Project-CSOM und verbindet die Anwendung und die PWA-Instanz. Alle Anforderungen an den Dienst verwenden den Projektkontext.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

Der Kontext benötigt den Verbindungsendpunkt, um eine Instanz in einer Anwendung zu erstellen. Der Verbindungsendpunkt ist die URL Ihrer PWA-Instanz. 
  
Das pwaECF-Wörterbuch speichert die Projekt-ECFs, die auf der PWA-Ebene definiert sind. Das Wörterbuch verwendet "ECF.InternalName" als Schlüssel und das "CustomField"-Objekt als Wert. Das Wörterbuch wird mit der "ListPWACustomFields"-Methode aufgefüllt und dann als Referenz in der "Main"-Methode verwendet. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>"Main"-Methode

Die "Main"-Methode verwaltet den Datenfluss der Anwendung. Wie bei anderen Anwendungen, in denen das Project Online-CSOM verwendet wird, initialisiert "Main" den Projektkontext. 
  
1. Rufen und Sie die ECFs in der Project Online-PWA-Instanz ab, und listen Sie sie auf.
    
   Diese Funktionalität ist in der "ListPWACustomFields"-Methode implementiert.
    
2. Rufen Sie Projekte mit benutzerdefinierten Feldern und nicht-benutzerdefinierten Feldern ab.
    
   Werden Projekte mit ECFs abgerufen, muss die Abfrageanforderung an den Project Online-Dienst die folgenden Elemente enthalten: 
    
   - **IncludeCustomFields** &ndash; Dieses Element fordert den Dienst auf, eine Sammlung veröffentlichter Projekte ("PublishedProject"-Objekte) zurückzugeben, wobei jedes veröffentlichte Projekt eine Erweiterung enthält, die benutzerdefinierte Felder unterstützt. Ist dieses Element nicht angegeben, gibt Project Online "PublishedProject"-Objekte zurück, die keine Daten aus benutzerdefinierten Feldern enthalten.
    
   - **IncludeCustomFields.CustomFields** &ndash; Dieses Element fordert den Dienst auf, die "PublishedProject"-Objekte mit "CustomFields"-Daten auszufüllen.
    
   Die folgende Anforderung gibt die Projekt-ID und den Projektnamen sowie die Objekterweiterung für benutzerdefinierte Felder und die Werte der benutzerdefinierten Felder an.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Überprüfen Sie jedes Projekt.
    
   Die in dieser Anwendung verwendeten Projektobjekte entsprechen dem "PublishedProject"-Typ, weil die Werte abgerufen und angezeigt werden. 
    
   Wenn Sie Datenwerte in einem oder mehreren Projekten aktualisieren müssen, würde das zu aktualisierende Projekt ausgecheckt, und würde die Anwendung ein "DraftProject"-Objekt verwenden, um die Werte abzurufen und das Projekt zu aktualisieren.
    
4. Zugreifen auf die ECF-Einträge für ein Projekt
    
   In jeder ECF-Instanz wird der Feldwert von den restlichen ECF-Informationen getrennt. Der Feldwert wird als Teil eines Schlüssel-Wert-Paares gespeichert. Die restlichen Informationen werden in einem "CustomField"-Objekt gespeichert.
    
   Zugreifen auf ECF-Werte in einem Projekt besteht aus zwei Teilen:
    
   - Durchlaufen der "CustomFields"-Sammlung
    
   - Zugreifen auf den richtigen Eintrag mit zwei Konstrukten
    
   In jedem Projekt werden zugewiesene ECF Einträge an zwei Stellen gespeichert: in einer "CustomFields"-Sammlung, die durchlaufen werden kann, und in den Feldwerten als Bestandteile von Schlüssel-Wert-Paaren. In den Schlüssel-Wert-Paaren ist der interne Name (internalName) der Schlüssel und der Feldwert der Wert. Verwenden Sie ein Wörterbuch, um die Feldwerte zu speichern und auf sie zuzugreifen. 
    
   Die ECF-Eigenschaften werden, anders als die Feldwerte, in "CustomField"-Objekten gespeichert, ein Objekt pro Projekt. Verwenden Sie eine "CustomFields"-Sammlung, um auf die ECFs zuzugreifen, die mit einem einzelnen Projekt verknüpft sind. 
    
5. In jedem Projekt werden die zugehörigen ECFs in einer Sammlung gespeichert, in der jeder Eintrag aus einem Schlüssel – der interne Name des ECF – und einem Objekt besteht, das den Wert des ECF enthält. Überführen Sie die Sammlung in ein Wörterbuch, um auf einzelne Einträge zuzugreifen. Die Deklaration folgt.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   Der Wert in einem Wörterbucheintrags entspricht dem Datentyp des ECF. Das Objekt für jedes ECF wird einem Typ aus einer Reihe von Typen zugeordnet. Für die meisten ECFs werden einfache Typen verwendet, die in Standardvariablen passen. Im folgenden Fragment wird gezeigt, dass verschiedene Typen eine minimale Verarbeitung erfordern:
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   Die Nachschlagetabelle von TEXT-Werten erfordert jedoch zusätzliche Verarbeitungsschritte. Die Anwendung ruft die entsprechende Nachschlagetabelle aus dem Dienst ab und gibt die ECF-Instanz (mit einem oder mehreren Werten) aus, indem sie die Nachschlagetabelle durchläuft. Im folgenden Codefragment wird die Verarbeitung von TEXT-ECFs gezeigt, einschließlich derjenigen mit einfachen Werten und derjenigen mit Nachschlagetabellen: 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   Diese Anwendung gibt schlicht den Wert oder die Werte aus. Allerdings ist es möglich, mehr Bedeutung aus den Datenwerten zu gewinnen.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

Die "ListPWACustomFields"-Methode ruft die ECFs ab, die mit Projekten verknüpft sind, und listet die ECFs auf. Diese Methode listet die ECFs auf, die in der PWA-Instanz registriert sind, die mit einzelnen Projekten verknüpft werden kann. Der Einstiegspunkt für Zugreifen auf die ECFs verwendet das "CustomFields"-Element des Projektkontexts, wie in der folgenden Abfrageanforderung:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

Die Methode überprüft nicht, ob für ein Projekt ein bestimmtes ECF verwendet wird.
  
## <a name="see-also"></a>Siehe auch

- [Project-Entwicklungsportal](https://developer.microsoft.com/de-DE/project)
- 
  [Übersicht: Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Hinzufügen oder Bearbeiten benutzerdefinierter Enterprise-Felder in Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

