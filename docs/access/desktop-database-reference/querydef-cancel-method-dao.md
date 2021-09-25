---
title: QueryDef.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6c404f493072974632bfdd155fc2664258721867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558044"
---
# <a name="querydefcancel-method-dao"></a>QueryDef.Cancel-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Abbrechen

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute-** oder **OpenConnection-Methodenaufrufs** zu beenden (das heißt, die Methode wurde mit der Option dbRunAsync aufgerufen). **Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.

