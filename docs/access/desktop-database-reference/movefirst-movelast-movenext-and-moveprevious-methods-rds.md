---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c78ea7f7b5ae34c291d9eab272cf893f3d073b95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558226"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)

**Gilt für**: Access 2013, Office 2013

Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*DataControl*. Recordset. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

Sie können die **Move-Methoden** mit **dem RDS verwenden. DataControl-Objekt** zum Navigieren durch die Datensätze in den datengebundenen Steuerelementen auf einer Webseite. 

For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object. You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**. You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively. The [Address Book example](address-book-navigation-buttons.md) shows how to do this.

