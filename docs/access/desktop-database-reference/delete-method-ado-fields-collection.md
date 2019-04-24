---
title: Delete-Methode (ADO Fields-Auflistung)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294106"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (ADO Fields-Auflistung)

**Gilt für**: Access 2013, Office 2013


Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Felder*. DELETE-*Feld*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Feld* |Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.|

## <a name="remarks"></a>Bemerkungen

Durch Aufrufen der **Fields.Delete**-Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.

