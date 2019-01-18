---
title: Delete-Methode (ADO-Fields-Auflistung)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718259"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (ADO-Fields-Auflistung)

**Betrifft**: Access 2013, Office 2013


Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Felder*. *Feld* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Field* |Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.|

## <a name="remarks"></a>Hinweise

Durch Aufrufen der **Fields.Delete** -Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.

