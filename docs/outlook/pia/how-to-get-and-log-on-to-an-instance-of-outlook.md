---
title: Abrufen einer Instanz von Outlook und Anmelden bei dieser
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-and-log-on-to-an-instance-of-outlook?redirectedfrom=MSDN
ms:contentKeyID: 55119926
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2cbf3f41ad7205111da63669e39bb7224d5f5fa0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590716"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Abrufen einer Instanz von Outlook und Anmelden bei dieser

In diesem Thema wird gezeigt, wie ein [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?redirectedfrom=MSDN&view=outlook-pia)-Objekt abgerufen wird, das eine aktive Instanz von Microsoft Outlook darstellt, falls eine Instanz auf dem lokalen Computer ausgeführt wird, oder wie eine neue Instanz von Outlook erstellt, die Anmeldung am Standardprofil durchgeführt und diese Instanz von Outlook zurückgegeben wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Helmut Obertanner hat das folgende Codebeispiel bereitgestellt. Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook. 

Die folgenden Codebeispiele enthalten die GetApplicationObject-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird. Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?redirectedfrom=MSDN&view=outlook-pia)-Namespace basiert.

Die GetApplicationObject-Methode verwendet Klassen in der .NET Framework-Klassenbibliothek, um alle Outlook-Prozesse zu prüfen und abzurufen, die auf dem lokalen Computer ausgeführt werden. Sie verwendet zunächst die [GetProcessesByName](https://docs.microsoft.com/dotnet/api/system.diagnostics.process.getprocessesbyname?redirectedfrom=MSDN&view=netframework-4.8#overloads)-Methode der [Process](https://docs.microsoft.com/dotnet/api/system.diagnostics.process?redirectedfrom=MSDN&view=netframework-4.8)-Klasse im [System.Diagnostics](https://docs.microsoft.com/dotnet/api/system.diagnostics?redirectedfrom=MSDN&view=netframework-4.8)-Namespace, um ein Array von Prozesskomponenten auf dem lokalen abzurufen, die den Prozessnamen „OUTLOOK“ aufweisen. Um zu überprüfen, ob das Array mindestens einen Outlook-Prozess enthält, verwendet GetApplicationObject Microsoft Language Integrated Query (LINQ). Die [Enumerable](https://msdn.microsoft.com/library/bb345746)-Klasse im [System.Linq](https://msdn.microsoft.com/library/bb336768)-Namespace bietet eine Reihe von Methoden, einschließlich der [Count](https://msdn.microsoft.com/library/bb357758)-Methode, welche die generische Schnittstelle [IEnumerable\<T\>](https://msdn.microsoft.com/library/9eekhta0) implementiert. Da die [Array](https://msdn.microsoft.com/library/czz5hkty)-Klasse die **IEnumerable(T)**-Schnittstelle implementiert, kann GetApplicationObject die **Count**-Methode auf das von **GetProcessesByName** zurückgegebene Array anwenden, um festzustellen, ob ein Outlook-Prozess ausgeführt wird. Ist dies der Fall verwendet GetApplicationObject die [GetActiveObject](https://msdn.microsoft.com/library/xt620x09)-Methode der [Marshal](https://msdn.microsoft.com/library/asx0thw2)-Klasse im [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\))-Namespace, um diese Instanz von Outlook abzurufen, und wandelt das Objekt in ein [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt für Outlook.

Wird Outlook auf dem lokalen Computer nicht ausgeführt, erstellt GetApplicationObject eine neue Instanz von Outlook, führt mithilfe der [Logon(Object, Object, Object, Object)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._namespace.logon?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__NameSpace_Logon_System_Object_System_Object_System_Object_System_Object_)-Methode des [NameSpace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.namespace?redirectedfrom=MSDN&view=outlook-pia)-Objekts die Anmeldung am Standardprofil durch und gibt diese neue Instanz von Outlook zurück.

Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die Anweisungen **Imports** oder **using** dürfen nicht direkt vor den Funktionen im Codebeispiel stehen, sondern müssen vor der öffentlichen Klassendeklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

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

