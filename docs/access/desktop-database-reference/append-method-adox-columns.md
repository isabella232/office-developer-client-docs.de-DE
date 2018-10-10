---
title: Append-Methode (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473114"
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
> <P>[!HINWEIS] Es tritt ein Fehler auf, wenn ein <STRONG>Column</STRONG> -Objekt an die <STRONG>Columns</STRONG> -Auflistung eines <A href="index-object-adox.md">Index</A>-Objekts angefügt wird und das <STRONG>Column</STRONG> -Objekt nicht in einem <A href="table-object-adox.md">Table</A>-Objekt vorhanden ist, das bereits an die <A href="tables-collection-adox.md">Tables</A>-Auflistung angefügt wurde.</P>


