---
title: Workspace.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ee787917a95e3716e629f87512caca1f408a6213
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617348"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **Workspace**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* .Close

*Ausdruck* Eine Variable, die ein **Workspace**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Eine Alternative zur **Close**-Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

