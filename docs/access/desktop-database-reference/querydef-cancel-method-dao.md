---
title: QueryDef. Cancel-Methode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301120"
---
# <a name="querydefcancel-method-dao"></a>QueryDef. Cancel-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Abbrechen

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute** -oder OpenConnection-Methodenaufrufs zu beenden (das heißt, die Methode wurde mit der dbRunAsync-Option aufgerufen). **** **Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.

