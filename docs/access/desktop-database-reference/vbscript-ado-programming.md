---
title: VBScript-ADO-Programmierung
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6336819b759e7ced832e993f72b05ebc2108587
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475623"
---
# <a name="vbscript-ado-programming"></a>VBScript-ADO-Programmierung


**Betrifft**: Access 2013 | Office 2013 

## <a name="creating-an-ado-project"></a>Erstellen eines ADO-Projekts

Da von Microsoft Visual Basic Scripting Edition keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in VBScript nicht definiert.

In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit VBScript verwendet werden können:

  - Verwenden, Sie für serverseitiges Skripting Adovbs.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Ado\\ Ordner standardmäßig.

  - Verwenden, Sie für clientseitiges Skripting Datei Adcvbs.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Msdac\\ Ordner standardmäßig.

Sie können entweder kopieren und Konstantendefinitionen aus diesen Dateien in ASP-Seiten einfügen, oder, wenn Sie serverseitiges Skripting, kopieren Adovbs.inc Datei in einen Ordner auf Ihrer Website und verweisen auf die sie über die ASP-Seite wie folgt:

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Erstellen von ADO-Objekten in VBScript

Sie können die **Dim** -Anweisung nicht zum Zuweisen von Objekten zu einem bestimmten Typ in VBScript verwenden. Außerdem wird in VBScript die Syntax **New**, die mit der **Dim** -Anweisung in Visual Basic für Applikationen verwendet wird, nicht unterstützt. Sie müssen stattdessen den **CreateObject** -Funktionsaufruf verwenden:

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

Konkretere VBScript-Beispiele sind in der ADO-Dokumentation enthalten. Weitere Informationen finden Sie unter [ADO-Codebeispiele in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Unterschiede zwischen VBScript und Visual Basic

Das Verwenden von ADO mit VBScript ist in vielerlei Hinsicht, z. B. hinsichtlich der Verwendung der Syntax, mit der Verwendung von ADO mit Visual Basic vergleichbar. Es sind jedoch einige erhebliche Unterschiede vorhanden:

- In VBScript wird nur der Datentyp Variant unterstützt, der verschiedene Datentypen enthalten kann. Sie können die benötigten Daten in einem Datentyp Variant speichern, und die Daten sind aufgrund der durch VBScript ausgeführten Umwandlung ordnungsgemäß funktionsfähig. Der für ADO erforderliche Typ wird erkannt, und der Wert in der Variante wird entsprechend konvertiert.

- Sie können keine `on error goto <label>` in VBScript.

- In VBScript werden einige der integrierten Visual Basic-Funktionen, wie z. B. **Msgbox**, **Date** und **IsNumeric**, unterstützt. Da es sich bei VBScript jedoch um eine Teilmenge von Visual Basic handelt, werden nicht alle integrierten Funktionen unterstützt. Beispielsweise werden in VBScript die **Format** -Funktion und die Datei-E/A-Funktionen nicht unterstützt.

