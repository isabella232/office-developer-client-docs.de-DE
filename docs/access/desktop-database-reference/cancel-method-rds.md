---
title: Cancel-Methode (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6d7c22f5b120d9685a2aae0b84eefc466bbfd7d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558608"
---
# <a name="cancel-method-rds"></a>Cancel-Methode (RDS)


**Gilt für**: Access 2013, Office 2013

Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen.

## <a name="syntax"></a>Syntax

*RDS*. *DataControl*. Abbrechen

## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie **Cancel** aufrufen, wird [ReadyState](readystate-property-rds.md) automatisch auf **adcReadyStateLoaded** festgelegt, und das [Recordset](recordset-object-ado.md)-Objekt ist leer.

