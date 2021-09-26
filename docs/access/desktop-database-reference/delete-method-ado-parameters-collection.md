---
title: Delete-Methode (Parameters-Auflistung in ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 30545ef12b5f794985b4925fe242e360ed1576f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622382"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete-Methode (Parameters-Auflistung in ADO)

**Gilt für**: Access 2013, Office 2013

Ein Objekt wird aus der [Parameters](parameters-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Parameter*. *Index* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Ein **String** -Wert, der den Namen des zu löschenden Objekts oder die Position des Objekts (Index) in der Auflistung enthält.|

## <a name="remarks"></a>Bemerkungen

Wenn Sie die **Delete**-Methode für eine Auflistung verwenden, können Sie eines der Objekte aus der Auflistung entfernen. Diese Methode steht nur für die **Parameters**-Auflistung eines [Command](command-object-ado.md)-Objekts zur Verfügung. Sie müssen die [Name](name-property-ado.md)-Eigenschaft des [Parameter](parameter-object-ado.md)-Objekts oder dessen Auflistungsindex verwenden, wenn Sie die **Delete**-Methode aufrufen. Eine Objektvariable ist kein gültiges Argument.

