---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cc1d03fe68093959406a444419128b161f3b5be4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921474"
---
# <a name="append-method-adox-keys"></a>Append-Methode (ADOX Keys)


**Betrifft**: Access 2013, Office 2013


Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Schlüssel*. Fügen Sie*Schlüssel* \[,*Schlüsseltyp* \] \[,*Spalte* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parameters

  - *Key*

  - Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.

  - *Schlüsseltyp*

  - Optional. Ein **Long** -Wert, der den Schlüsseltyp angibt. Der Parameter *Schlüssel* entspricht der [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) -Eigenschaft eines **Key** -Objekts.

  - *Column*

  - Optional. Ein **String** -Wert, der den Namen der zu indizierenden Spalte angibt. Der *Columns* -Parameter entspricht dem Wert der [Name](name-property-adox.md) -Eigenschaft eines [Column](column-object-adox.md) -Objekts.

  - *RelatedTable*

  - Optional. Ein **String** -Wert, der den Namen der verknüpften Tabelle angibt. Der Parameter *RelatedTable* entspricht dem Wert der **Name** -Eigenschaft eines [Table](table-object-adox.md) -Objekts.

  - *RelatedColumn*

  - Optional. Ein String-Wert, der den Namen der verknüpften Spalte für einen Fremdschlüssel angibt. Der RelatedColumn-Parameter entspricht dem Wert der Name-Eigenschaft eines Column-Objekts.

## <a name="remarks"></a>Hinweise

Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.

