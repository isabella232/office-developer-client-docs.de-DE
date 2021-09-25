---
title: Importieren von Termin-XML-Daten in Outlook-Terminobjekte
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fef3e924ed5f81d5d64e5ca77bc417c000866ad2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560508"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>Importieren von Termin-XML-Daten in Outlook-Terminobjekte

In diesem Thema wird gezeigt, wie Termindaten im XML-Format gelesen, die Daten in Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekten im Standardkalender gespeichert und die Terminobjekte in einem Array zurückgegeben werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Helmut Obertanner hat das folgende Codebeispiel bereitgestellt. Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook. 


Die folgenden Codebeispiele enthalten die CreateAppointmentsFromXml-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird. Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert.

Die CreateAppointmentsFromXml-Methode akzeptiert zwei Eingabeparameter:

  - application ist ein vertrauenswürdiges [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt von Outlook.

  - xml ist entweder eine XML-Zeichenfolge oder eine Zeichenfolge, die einen Pfad zu einer gültigen XML-Datei darstellt. In den folgenden Codebeispielen begrenzt der XML-Code Termindaten mithilfe der folgenden XML-Tags:
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Termindaten</p></th>
    <th><p>Trennendes XML-Tag</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Gesamter Satz an Termindaten</p></td>
    <td><p>Termine</p></td>
    </tr>
    <tr class="even">
    <td><p>Jeder Termine in der Gruppe</p></td>
    <td><p>Termin</p></td>
    </tr>
    <tr class="odd">
    <td><p>Startzeit eines Termins</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>Endzeit eines Termins</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>Titel eines Termins</p></td>
    <td><p>Betreff</p></td>
    </tr>
    <tr class="even">
    <td><p>Ort eines Termins</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>Details eines Termins</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


Das folgende Beispiel zeigt Eingabedaten für den *xml*-Parameter.

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

Die CreateAppointmentsFromXml-Methode arbeitet mit der Microsoft COM-Implementierung des XML-Dokumentobjektmodells (DOM) zum Laden und Verarbeiten der XML-Daten, die xml bereitstellt. CreateAppointmentsFromXml überprüft zuerst, ob xml eine gültige XML-Datenquelle angibt. Falls ja, werden die Daten in ein XML-Dokument ([DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\))) geladen. Andernfalls löst CreateAppointmentsFromXml eine Ausnahme aus. Weitere Informationen zum XML-DOM finden Sie unter [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).

Für jeden untergeordneten Terminknoten, der vom appointment-Tag in den XML-Daten begrenzt wird, sucht CreateAppointmentsFromXml nach spezifischen Tags, verwendet das DOM zum Extrahieren der Daten und weist die Daten den entsprechenden Eigenschaften eines **AppointmentItem**-Objekts zu: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) und [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)). CreateAppointmentsFromXml speichert anschließend den Termin im Standardkalender.

CreateAppointmentsFromXml verwendet die [Add-Methode](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) der [ \<T\> List-Klasse](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) im [System.Collections.Generic-Namespace,](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) um diese AppointmentItem-Objekte zu aggregieren. Wenn die Methode alle Termine in den XML-Daten verarbeitet hat, gibt sie die AppointmentItem-Objekte in einem Array zurück.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

