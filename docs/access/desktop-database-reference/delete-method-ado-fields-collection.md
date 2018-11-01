---
title: Delete-Methode (Fields-Auflistung in ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886396"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (Fields-Auflistung in ADO)


**Betrifft**: Access 2013, Office 2013



Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Felder*. *Feld* löschen

## <a name="parameters"></a>Parameter

  - *Field*

  - Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.

## <a name="remarks"></a>Hinweise

Durch Aufrufen der **Fields.Delete** -Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.

