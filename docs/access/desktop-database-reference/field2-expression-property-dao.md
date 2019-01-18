---
title: Field2.Expression-Eigenschaft (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720086"
---
# <a name="field2expression-property-dao"></a>Field2.Expression-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Ruft ab oder legt diesen fest einen Ausdruck, der die Formel für ein berechnetes Feld darstellt. **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Access 2010

## <a name="syntax"></a>Syntax

*Ausdruck* . Ausdruck

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

In Access 2013 können Sie Felder der Tabelle erstellen, die Werte berechnen. Die Berechnung können Werte aus Feldern in derselben Tabelle als auch integrierte Funktionen enthalten.

Die Berechnung kann keine Felder aus anderen Tabellen oder Abfragen enthalten.

Die Ergebnisse der Berechnung sind schreibgeschützt.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

