---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297088"
---
# <a name="append-method-adox-keys"></a>Append-Methode (ADOX Keys)

**Gilt für**: Access 2013, Office 2013

Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Schlüssel*. Append *-Taste* \[, KeyType** \] \[,*Column* \] \[,*relatedable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Key* |Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.|
|*KeyType* |Optional. Ein **Long**-Wert, der den Schlüsseltyp angibt. Der *Key*-Parameter entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft eines **Key**-Objekts.|
|*Spalte* |Optional. Ein **String**-Wert, der den Namen der zu indizierenden Spalte angibt. Der *Columns*-Parameter entspricht dem Wert der [Name](name-property-adox.md)-Eigenschaft eines [Column](column-object-adox.md)-Objekts.|
|*RelatedTable* |Optional. Ein **String**-Wert, der den Namen der verknüpften Tabelle angibt. Der *RelatedTable*-Parameter entspricht dem Wert der **Name**-Eigenschaft eines [Table](table-object-adox.md)-Objekts.|
|*RelatedColumn* |Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.|

## <a name="remarks"></a>Bemerkungen

Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.

