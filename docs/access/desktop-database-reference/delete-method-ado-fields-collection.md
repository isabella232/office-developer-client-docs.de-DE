---
title: Delete-Methode (Fields-Auflistung in ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474618"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (Fields-Auflistung in ADO)


**Betrifft**: Access 2013 | Office 2013



Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.

## <a name="syntax"></a>Syntax

*Felder*. *Feld* löschen

## <a name="parameters"></a>Parameter

  - *Field*

  - Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.

## <a name="remarks"></a>Hinweise

Durch Aufrufen der **Fields.Delete** -Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.

