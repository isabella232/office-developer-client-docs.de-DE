---
title: Field2.Expression-Eigenschaft (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c03310159915fd7bbb0804582d8f3967d40fb9b2
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937652"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="6006c-102">Field2.Expression-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6006c-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="6006c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6006c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6006c-104">Ruft ab oder legt diesen fest einen Ausdruck, der die Formel für ein berechnetes Feld darstellt.</span><span class="sxs-lookup"><span data-stu-id="6006c-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="6006c-105">Lese-/Schreibzugriff **String**.</span><span class="sxs-lookup"><span data-stu-id="6006c-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="6006c-106">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="6006c-106">Version information</span></span>

<span data-ttu-id="6006c-107">Hinzugefügte Version: Access 2010</span><span class="sxs-lookup"><span data-stu-id="6006c-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="6006c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6006c-108">Syntax</span></span>

<span data-ttu-id="6006c-109">*Ausdruck* . Ausdruck</span><span class="sxs-lookup"><span data-stu-id="6006c-109">*expression* .Expression</span></span>

<span data-ttu-id="6006c-110">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6006c-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6006c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6006c-111">Remarks</span></span>

<span data-ttu-id="6006c-112">In Access 2013 können Sie Felder der Tabelle erstellen, die Werte berechnen.</span><span class="sxs-lookup"><span data-stu-id="6006c-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="6006c-113">Die Berechnung können Werte aus Feldern in derselben Tabelle als auch integrierte Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6006c-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="6006c-114">Die Berechnung kann keine Felder aus anderen Tabellen oder Abfragen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6006c-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="6006c-115">Die Ergebnisse der Berechnung sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6006c-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="6006c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6006c-116">Example</span></span>

<span data-ttu-id="6006c-p103">Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.</span><span class="sxs-lookup"><span data-stu-id="6006c-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="6006c-120">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6006c-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

