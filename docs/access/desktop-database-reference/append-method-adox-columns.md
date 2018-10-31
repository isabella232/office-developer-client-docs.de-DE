---
title: Append-Methode (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861575"
---
# <a name="append-method-adox-columns"></a>Append-Methode (ADOX Columns)


**Betrifft**: Access 2013 | Office 2013

Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Spalten*. Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parameter

  - *Column*

  - Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.

  - *Type*

  - Optional. Ein **Long** -Wert, der den Datentyp der Spalte angibt. Die [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.

  - *DefinedSize*

  - Optional. Ein **Long** -Wert, der die Größe einer Spalte angibt. Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.


> [!NOTE]
> [!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.


