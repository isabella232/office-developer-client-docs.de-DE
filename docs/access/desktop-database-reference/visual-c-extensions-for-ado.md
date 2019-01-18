---
title: Visual C++-Erweiterungen für ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720233"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="bfadb-102">Visual C++-Erweiterungen für ADO</span><span class="sxs-lookup"><span data-stu-id="bfadb-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="bfadb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfadb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfadb-104">Die bevorzugte Methode zum Programmieren von ADO mit Visual C++ wird mithilfe der \*\* \#importieren\*\* Richtlinie, wie in [Microsoft Visual C++-ADO-Programmierung](visual-c-ado-programming.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="bfadb-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="bfadb-105">Jedoch frühere Versionen von ADO mit einer alternativen Methode der-Programmierung mit Visual C++ geliefert: die Visual C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="bfadb-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="bfadb-106">Dieser Abschnitt beschreibt dieses Feature für diejenigen, die Visual C++-Erweiterungen Code verwalten müssen, aber neuer ADO-Code geschrieben werden soll, mithilfe von \# **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="bfadb-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="bfadb-p102">Eine der mühsamsten Aufgaben, der sich Visual C++-Programmierer beim Abrufen von Daten mit ADO gegenübersehen, ist das Konvertieren der als VARIANT-Datentyp zurückgegebenen Daten in einen C++-Datentyp und das anschließende Speichern der konvertierten Daten in einer Klasse oder Struktur. Das Abrufen von C++-Daten über einen VARIANT-Datentyp ist nicht nur aufwändig, sondern es verringert auch die Leistung.</span><span class="sxs-lookup"><span data-stu-id="bfadb-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="bfadb-p103">In ADO wird eine Schnittstelle bereitgestellt, die das Abrufen von Daten in systemeigene C/C++-Datentypen ohne Verwendung eines VARIANT-Datentyps unterstützt und außerdem Präprozessormakros bereitstellt, durch die die Verwendung der Schnittstelle vereinfacht wird. Das Ergebnis ist ein flexibles Tool, das einfacher zu verwenden ist und über eine gute Leistung verfügt.</span><span class="sxs-lookup"><span data-stu-id="bfadb-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="bfadb-p104">Ein gängiges C/C++-Clientszenario ist das Binden eines Datensatzes in einem [Recordset](recordset-object-ado.md) an eine C/C++-Struktur oder -Klasse, die systemeigene C/C++-Typen enthält. Bei Verwendung von VARIANTs gehört hierzu das Schreiben von Code für die Konvertierung von VARIANT-Typen in systemeigene C/C++-Typen. Die Visual C++-Erweiterungen für ADO sollen dieses Szenario für Visual C++-Programmierer deutlich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="bfadb-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="bfadb-114">Unter den folgenden Themen finden Sie weitere Informationen zu den Visual C++-Erweiterungen für ADO.</span><span class="sxs-lookup"><span data-stu-id="bfadb-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="bfadb-115">Verwenden von Visual C++-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="bfadb-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="bfadb-116">Visual C++-Erweiterungsheader</span><span class="sxs-lookup"><span data-stu-id="bfadb-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="bfadb-117">Visual C++-Erweiterungen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="bfadb-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

