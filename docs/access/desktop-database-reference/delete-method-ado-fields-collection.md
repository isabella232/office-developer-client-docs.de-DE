---
title: Delete-Methode (ADO Fields-Auflistung)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 463056a45ce3636d6b215c03fd65e8614f633bf3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577444"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (ADO Fields-Auflistung)

**Gilt für**: Access 2013, Office 2013


Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Felder*. *Feld* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Feld* |Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.|

## <a name="remarks"></a>HinwBemerkungeneise

Durch Aufrufen der **Fields.Delete**-Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.

