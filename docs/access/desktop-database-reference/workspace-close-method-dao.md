---
title: Workspace.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708627"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Schließt ein geöffnetes **Workspace**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Schließen Sie

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).

