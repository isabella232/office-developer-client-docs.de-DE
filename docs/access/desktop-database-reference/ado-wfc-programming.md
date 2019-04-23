---
title: ADO/WFC-Programmierung
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 904b5e3930c0e7e7b1d98f94bd39cfbf816aa145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283205"
---
# <a name="adowfc-programming"></a><span data-ttu-id="cca12-102">ADO/WFC-Programmierung</span><span class="sxs-lookup"><span data-stu-id="cca12-102">ADO/WFC programming</span></span>

<span data-ttu-id="cca12-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cca12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cca12-p101">ADO wurde für Microsoft Visual J++ 6.0 so erweitert, dass auf folgende Weise die Zusammenarbeit mit Windows Foundation Classes (WFC) möglich ist. Erstens wurde ein Satz von Java-Klassen implementiert, durch den die ADO-Schnittstellen erweitert und für den Java-Programmierer interessante Benachrichtigungen erstellt werden. Außerdem machen die Java-Klassen Funktionen verfügbar, durch die Java-Typen an den Benutzer zurückgegeben werden. Zur Verbesserung der Leistung wird durch die Java-Klasse direkt auf die systemeigenen Datentypen im rowset-OLE DB-Objekt zugegriffen, die an den Java-Programmierer zurückgegeben werden, ohne erst in eine bzw. aus einer Variante konvertiert zu werden. ADO wurde außerdem erweitert, um mit Ereignisbenachrichtigungen im WFC-Framework zusammenzuarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cca12-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="cca12-p102">ADO für Windows Foundation Classes (ADO/WFC) unterstützt alle ADO-Standardmethoden, -eigenschaften, -objekte und -ereignisse. Operationen, für die eine Variante als Parameter erforderlich ist und die in einer Sprache wie Microsoft Visual Basic hervorragende Leistung bieten, zeigen in einer Sprache wie Visual J++ eine geringere Leistung. Aus diesem Grund werden von ADO/WFC Accessorfunktionen für das [Field](field-object-ado.md)-Objekt bereitgestellt, für die systemeigene Java-Datentypen anstelle der Variantendatentypen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cca12-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="cca12-111">Ausführlichere Informationen in der ADO-Dokumentation zu den ADO/WFC-Paketen finden Sie unter [dem ADO/WFC-Syntaxindex](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).</span><span class="sxs-lookup"><span data-stu-id="cca12-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="cca12-112">Verweisen auf die Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cca12-112">Referencing the library</span></span>

<span data-ttu-id="cca12-113">Fügen Sie die folgende Zeile in den Code ein, um die ADO/WFC-Datenklassen in das Projekt zu importieren:</span><span class="sxs-lookup"><span data-stu-id="cca12-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

