---
title: State-Eigenschaft (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5e6d8dbad4245e68fb18cbc5c90dab54d4466601
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593544"
---
# <a name="state-property-ado-md"></a>State-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt den aktuellen Status der Zellmenge an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen ganzzahligen, schreibgeschützten **Long**-Wert zurück, der den aktuellen Status des [Cellset](cellset-object-ado-md.md)-Objekts angibt. Die folgenden Werte sind gültig: **adStateClosed** (0) und **adStateOpen** (1).

## <a name="remarks"></a>HinwBemerkungeneise

Verweisen Sie in dem Projekt auf die ADO-Typbibliothek verweisen, um die [ObjectStateEnum](objectstateenum.md)-Konstantennamen zu verwenden. Weitere Informationen hierzu finden Sie unter [Verwenden von ADO mit ADO MD](using-ado-with-ado-md.md) .

