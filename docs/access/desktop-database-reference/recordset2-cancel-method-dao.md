---
title: Recordset2.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a7fbf84e610f57081bea30a0b6a609a11d865f13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611749"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Abbrechen

*Ausdruck* Ein Ausdruck, der ein **Recordset2-Objekt** zurückgibt.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute-** oder **OpenConnection-Methodenaufrufs** zu beenden (das heißt, die Methode wurde mit der Option dbRunAsync aufgerufen). **Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.

