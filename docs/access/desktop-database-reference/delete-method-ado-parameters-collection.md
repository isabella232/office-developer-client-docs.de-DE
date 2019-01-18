---
title: Delete-Methode (ADO-Parameters-Auflistung)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704574"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete-Methode (ADO-Parameters-Auflistung)

**Betrifft**: Access 2013, Office 2013

Ein Objekt wird aus der [Parameters](parameters-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Parameter*. *Index* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Ein **String** -Wert, der den Namen des zu löschenden Objekts oder die Position des Objekts (Index) in der Auflistung enthält.|

## <a name="remarks"></a>Hinweise

Wenn Sie die **Delete** -Methode für eine Auflistung verwenden, können Sie eines der Objekte aus der Auflistung entfernen. Diese Methode steht nur für die **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts zur Verfügung. Sie müssen die [Name](parameter-object-ado.md)-Eigenschaft des [Parameter](name-property-ado.md)-Objekts oder dessen Auflistungsindex verwenden, wenn Sie die **Delete** -Methode aufrufen. Eine Objektvariable ist kein gültiges Argument.

