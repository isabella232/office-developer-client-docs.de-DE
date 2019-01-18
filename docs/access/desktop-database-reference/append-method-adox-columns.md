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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711231"
---
# <a name="append-method-adox-columns"></a>Append-Methode (ADOX Columns)

**Betrifft**: Access 2013, Office 2013

Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Spalten*. Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Column* |Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.|
|*Type* |Optional. Ein **Long** -Wert, der den Datentyp der Spalte angibt. Die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.|
|*DefinedSize* |Optional. Ein **Long** -Wert, der die Größe einer Spalte angibt. Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.|


> [!NOTE]
> [!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.


