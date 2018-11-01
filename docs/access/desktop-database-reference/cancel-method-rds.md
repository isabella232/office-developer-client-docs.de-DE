---
title: Cancel-Methode (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868746"
---
# <a name="cancel-method-rds"></a>Cancel-Methode (RDS)


**Betrifft**: Access 2013, Office 2013

Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.

## <a name="syntax"></a>Syntax

*RDS*. *DataControl*. Abbrechen

## <a name="remarks"></a>Hinweise

Wenn Sie **Cancel** aufrufen, wird [ReadyState](readystate-property-rds.md) automatisch auf **adcReadyStateLoaded** festgelegt, und das [Recordset](recordset-object-ado.md)-Objekt ist leer.

