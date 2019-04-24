---
title: Recordset2. Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307413"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2. Cancel-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Abbrechen

*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute** -oder OpenConnection-Methodenaufrufs zu beenden (das heißt, die Methode wurde mit der dbRunAsync-Option aufgerufen). **** **Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.

