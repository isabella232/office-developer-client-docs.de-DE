---
title: Append-Methode (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297123"
---
# <a name="append-method-adox-columns"></a>Append-Methode (ADOX Columns)

**Gilt für**: Access 2013, Office 2013

Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Spalten*. Append-*Spalte* \[,*Type* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Column* |Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.|
|*Type* |Optional. Ein **Long**-Wert, der den Datentyp der Spalte angibt. Der *Type*-Parameter entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)-Eigenschaft eines **Column**-Objekts.|
|*DefinedSize* |Optional. Ein **Long**-Wert, der die Größe einer Spalte angibt. Der *DefinedSize*-Parameter entspricht der [DefinedSize](definedsize-property-adox.md)-Eigenschaft eines **Column**-Objekts.|


> [!NOTE]
> Es tritt ein Fehler auf, wenn ein **Column**-Objekt an die **Columns**-Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column**-Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.


