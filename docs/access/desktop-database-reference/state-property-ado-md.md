---
title: State-Eigenschaft (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306363"
---
# <a name="state-property-ado-md"></a>State-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt den aktuellen Status der Zellmenge an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen ganzzahligen, schreibgeschützten **Long**-Wert zurück, der den aktuellen Status des [Cellset](cellset-object-ado-md.md)-Objekts angibt. Die folgenden Werte sind gültig: **adStateClosed** (0) und **adStateOpen** (1).

## <a name="remarks"></a>Bemerkungen

Verweisen Sie in dem Projekt auf die ADO-Typbibliothek verweisen, um die [ObjectStateEnum](objectstateenum.md)-Konstantennamen zu verwenden. Weitere Informationen hierzu finden Sie unter [Verwenden von ADO mit ADO MD](using-ado-with-ado-md.md) .

