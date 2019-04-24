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
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a><span data-ttu-id="decf1-102">Abrufen einer Instanz von Outlook und Anmelden bei dieser</span><span class="sxs-lookup"><span data-stu-id="decf1-102">Get and sign in to an instance of Outlook</span></span>

<span data-ttu-id="decf1-103">In diesem Thema wird gezeigt, wie ein [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt abgerufen wird, das eine aktive Instanz von Microsoft Outlook darstellt, falls eine Instanz auf dem lokalen Computer ausgeführt wird, oder wie eine neue Instanz von Outlook erstellt, die Anmeldung am Standardprofil durchgeführt und diese Instanz von Outlook zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="decf1-103">This topic shows how to obtain an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Microsoft Outlook, if there is one running on the local computer, or to create a new instance of Outlook, sign in to the default profile, and return that instance of Outlook.</span></span>

## <a name="example"></a><span data-ttu-id="decf1-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="decf1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="decf1-105">Helmut Obertanner hat das folgende Codebeispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="decf1-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="decf1-106">Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook.</span><span class="sxs-lookup"><span data-stu-id="decf1-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="decf1-107">Die folgenden Codebeispiele enthalten die GetApplicationObject-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="decf1-107">The following code examples contain the GetApplicationObject method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="decf1-108">Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert.</span><span class="sxs-lookup"><span data-stu-id="decf1-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="decf1-109">Die GetApplicationObject-Methode verwendet Klassen in der .NET Framework-Klassenbibliothek, um alle Outlook-Prozesse zu prüfen und abzurufen, die auf dem lokalen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="decf1-109">The GetApplicationObject method uses classes in the .NET Framework class library to check and obtain any Outlook process running on the local computer.</span></span> <span data-ttu-id="decf1-110">Sie verwendet zunächst die [GetProcessesByName](https://msdn.microsoft.com/de-DE/library/wbt7d3cy)-Methode der [Process](https://msdn.microsoft.com/de-DE/library/ccf1tfx0)-Klasse im [System.Diagnostics](https://msdn.microsoft.com/de-DE/library/15t15zda)-Namespace, um ein Array von Prozesskomponenten auf dem lokalen abzurufen, die den Prozessnamen „OUTLOOK“ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="decf1-110">It first uses the [GetProcessesByName](https://msdn.microsoft.com/de-DE/library/wbt7d3cy) method of the [Process](https://msdn.microsoft.com/de-DE/library/ccf1tfx0) class in the [System.Diagnostics](https://msdn.microsoft.com/de-DE/library/15t15zda) namespace to obtain an array of process components on the local computer that share the process name "OUTLOOK".</span></span> <span data-ttu-id="decf1-111">Um zu überprüfen, ob das Array mindestens einen Outlook-Prozess enthält, verwendet GetApplicationObject Microsoft Language Integrated Query (LINQ).</span><span class="sxs-lookup"><span data-stu-id="decf1-111">To check whether the array does contain at least one Outlook process, GetApplicationObject uses Microsoft Language Integrated Query (LINQ).</span></span> <span data-ttu-id="decf1-112">Die [Enumerable](https://msdn.microsoft.com/de-DE/library/bb345746)-Klasse im [System.Linq](https://msdn.microsoft.com/de-DE/library/bb336768)-Namespace bietet eine Reihe von Methoden, einschließlich der [Count](https://msdn.microsoft.com/de-DE/library/bb357758)-Methode, die die generische [IEnumerable\<T\>](https://msdn.microsoft.com/de-DE/library/9eekhta0)-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="decf1-112">The [Enumerable](https://msdn.microsoft.com/de-DE/library/bb345746) class in the [System.Linq](https://msdn.microsoft.com/de-DE/library/bb336768) namespace provides a set of methods, including the [Count](https://msdn.microsoft.com/de-DE/library/bb357758) method, that implement the [IEnumerable\<T\>](https://msdn.microsoft.com/de-DE/library/9eekhta0) generic interface.</span></span> <span data-ttu-id="decf1-113">Da die [Array](https://msdn.microsoft.com/de-DE/library/czz5hkty)-Klasse die **IEnumerable(T)**-Schnittstelle implementiert, kann GetApplicationObject die **Count**-Methode auf das von \*\* GetProcessesByName\*\* zurückgegebene Array anwenden, um festzustellen, ob ein Outlook-Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="decf1-113">Because the [Array](https://msdn.microsoft.com/de-DE/library/czz5hkty) class implements the **IEnumerable(T)** interface, GetApplicationObject can apply the **Count** method to the array returned by **GetProcessesByName** to see whether there is an Outlook process running.</span></span> <span data-ttu-id="decf1-114">Ist dies der Fall verwendet GetApplicationObject die [GetActiveObject](https://msdn.microsoft.com/de-DE/library/xt620x09)-Methode der [Marshal](https://msdn.microsoft.com/de-DE/library/asx0thw2)-Klasse im [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\))-Namespace, um diese Instanz von Outlook abzurufen, und wandelt das Objekt in ein [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt für Outlook.</span><span class="sxs-lookup"><span data-stu-id="decf1-114">If there is, GetApplicationObject uses the [GetActiveObject](https://msdn.microsoft.com/de-DE/library/xt620x09) method of the [Marshal](https://msdn.microsoft.com/de-DE/library/asx0thw2) class in the [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) namespace to obtain that instance of Outlook, and casts that object to an Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

<span data-ttu-id="decf1-115">Wird Outlook auf dem lokalen Computer nicht ausgeführt, erstellt GetApplicationObject eine neue Instanz von Outlook, führt mithilfe der [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts die Anmeldung am Standardprofil durch und gibt diese neue Instanz von Outlook zurück.</span><span class="sxs-lookup"><span data-stu-id="decf1-115">If Outlook is not running on the local computer, GetApplicationObject creates a new instance of Outlook, uses the [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to sign in to the default profile, and returns that new instance of Outlook.</span></span>

<span data-ttu-id="decf1-116">Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="decf1-116">The following is the Visual Basic code example, followed by the C\# code example.</span></span>

<span data-ttu-id="decf1-117">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="decf1-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="decf1-118">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="decf1-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="decf1-119">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="decf1-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="decf1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="decf1-120">See also</span></span>

- [<span data-ttu-id="decf1-121">Sitzungen</span><span class="sxs-lookup"><span data-stu-id="decf1-121">Sessions</span></span>](sessions.md)

