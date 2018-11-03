---
title: Delete-Methode (ADO-Parameters-Auflistung)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944872"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete-Methode (ADO-Parameters-Auflistung)


**Betrifft**: Access 2013, Office 2013


Ein Objekt wird aus der [Parameters](parameters-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Parameter*. *Index* löschen

## <a name="parameters"></a>Parameter

- *Index*

  - Ein **String** -Wert, der den Namen des zu löschenden Objekts oder die Position des Objekts (Index) in der Auflistung enthält.

## <a name="remarks"></a>Hinweise

Wenn Sie die **Delete** -Methode für eine Auflistung verwenden, können Sie eines der Objekte aus der Auflistung entfernen. Diese Methode steht nur für die **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts zur Verfügung. Sie müssen die [Name](parameter-object-ado.md)-Eigenschaft des [Parameter](name-property-ado.md)-Objekts oder dessen Auflistungsindex verwenden, wenn Sie die **Delete** -Methode aufrufen. Eine Objektvariable ist kein gültiges Argument.

