---
title: VBScript-ADO-Programmierung
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4aff2c8b3394321367851ad82e4e7efe98badff8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306027"
---
# <a name="vbscript-ado-programming"></a>VBScript-ADO-Programmierung


**Gilt für**: Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Erstellen eines ADO-Projekts

Da von Microsoft Visual Basic Scripting Edition keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in VBScript nicht definiert.

In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit VBScript verwendet werden können:

  - Für die serverseitige Skripterstellung verwenden Sie Datei Adovbs. Inc, die standardmäßig im Ordner\\c:\\Program Files\\Common\\Files\\ System ADO installiert ist.

  - Für die clientseitige Skripterstellung verwenden Sie die Datei "addcvbs. Inc", die\\standardmäßig\\im Ordner\\"\\c\\ : Program Files System msdac" installiert ist.

Sie können entweder kopieren und Einfügen von Konstanten Definitionen aus diesen Dateien in Ihre ASP-Seiten oder, wenn Sie serverseitige Skripterstellung durchführen, kopieren Sie die Datei Datei Adovbs. Inc in einen Ordner auf Ihrer Website, und verweisen Sie auf Ihrer ASP-Seite wie folgt:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Erstellen von ADO-Objekten in VBScript

Sie können die **Dim**-Anweisung nicht zum Zuweisen von Objekten zu einem bestimmten Typ in VBScript verwenden. Außerdem wird in VBScript die Syntax **New**, die mit der **Dim**-Anweisung in Visual Basic für Applikationen verwendet wird, nicht unterstützt. Sie müssen stattdessen den **CreateObject**-Funktionsaufruf verwenden:

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>VBScript (Beispiele)

Der folgende Code ist ein allgemeines Beispiel für die serverseitige VBScript-Programmierung in einer ASP-Datei (Active Server Pages):

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

Konkretere VBScript-Beispiele sind in der ADO-Dokumentation enthalten. Weitere Informationen finden Sie unter [ADO-Codebeispiele in Microsoft Visual Basic scriptIng Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Unterschiede zwischen VBScript und Visual Basic

Das Verwenden von ADO mit VBScript ist in vielerlei Hinsicht, z. B. hinsichtlich der Verwendung der Syntax, mit der Verwendung von ADO mit Visual Basic vergleichbar. Es sind jedoch einige erhebliche Unterschiede vorhanden:

- VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.

- Sie können nicht `on error goto <label>` innerhalb von VBScript verwenden.

- In VBScript werden einige der integrierten Visual Basic-Funktionen, wie z. B. **Msgbox**, **Date** und **IsNumeric**, unterstützt. Da es sich bei VBScript jedoch um eine Teilmenge von Visual Basic handelt, werden nicht alle integrierten Funktionen unterstützt. Beispielsweise werden in VBScript die **Format** -Funktion und die Datei-E/A-Funktionen nicht unterstützt.

