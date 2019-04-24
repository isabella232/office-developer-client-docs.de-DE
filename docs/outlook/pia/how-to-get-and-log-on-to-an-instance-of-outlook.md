---
title: Abrufen einer Instanz von Outlook und Anmelden bei dieser
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4445d0665ea5a3d36a5ff7c92b5a46cfe4fffaa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320272"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Abrufen einer Instanz von Outlook und Anmelden bei dieser

In diesem Thema wird gezeigt, wie ein [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt abgerufen wird, das eine aktive Instanz von Microsoft Outlook darstellt, falls eine Instanz auf dem lokalen Computer ausgeführt wird, oder wie eine neue Instanz von Outlook erstellt, die Anmeldung am Standardprofil durchgeführt und diese Instanz von Outlook zurückgegeben wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Helmut Obertanner hat das folgende Codebeispiel bereitgestellt. Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook. 

Die folgenden Codebeispiele enthalten die GetApplicationObject-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird. Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert.

Die GetApplicationObject-Methode verwendet Klassen in der .NET Framework-Klassenbibliothek, um alle Outlook-Prozesse zu prüfen und abzurufen, die auf dem lokalen Computer ausgeführt werden. Sie verwendet zunächst die [GetProcessesByName](https://msdn.microsoft.com/de-DE/library/wbt7d3cy)-Methode der [Process](https://msdn.microsoft.com/de-DE/library/ccf1tfx0)-Klasse im [System.Diagnostics](https://msdn.microsoft.com/de-DE/library/15t15zda)-Namespace, um ein Array von Prozesskomponenten auf dem lokalen abzurufen, die den Prozessnamen „OUTLOOK“ aufweisen. Um zu überprüfen, ob das Array mindestens einen Outlook-Prozess enthält, verwendet GetApplicationObject Microsoft Language Integrated Query (LINQ). Die [Enumerable](https://msdn.microsoft.com/de-DE/library/bb345746)-Klasse im [System.Linq](https://msdn.microsoft.com/de-DE/library/bb336768)-Namespace bietet eine Reihe von Methoden, einschließlich der [Count](https://msdn.microsoft.com/de-DE/library/bb357758)-Methode, die die generische [IEnumerable\<T\>](https://msdn.microsoft.com/de-DE/library/9eekhta0)-Schnittstelle implementieren. Da die [Array](https://msdn.microsoft.com/de-DE/library/czz5hkty)-Klasse die **IEnumerable(T)**-Schnittstelle implementiert, kann GetApplicationObject die **Count**-Methode auf das von ** GetProcessesByName** zurückgegebene Array anwenden, um festzustellen, ob ein Outlook-Prozess ausgeführt wird. Ist dies der Fall verwendet GetApplicationObject die [GetActiveObject](https://msdn.microsoft.com/de-DE/library/xt620x09)-Methode der [Marshal](https://msdn.microsoft.com/de-DE/library/asx0thw2)-Klasse im [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\))-Namespace, um diese Instanz von Outlook abzurufen, und wandelt das Objekt in ein [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt für Outlook.

Wird Outlook auf dem lokalen Computer nicht ausgeführt, erstellt GetApplicationObject eine neue Instanz von Outlook, führt mithilfe der [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts die Anmeldung am Standardprofil durch und gibt diese neue Instanz von Outlook zurück.

Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>Siehe auch

- [Sitzungen](sessions.md)

