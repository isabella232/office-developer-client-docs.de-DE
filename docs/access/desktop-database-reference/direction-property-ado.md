---
title: Direction-Eigenschaft (ADO)
TOCTitle: Direction Property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611e5efbe53964c5ba255380e2659f024bd6be9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474622"
---
# <a name="direction-property-ado"></a>Direction-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter oder einen Ein- und Ausgabeparameter darstellt, oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert festgelegt oder zurückgegeben.

## <a name="remarks"></a>Hinweise

Mit der **Direction** -Eigenschaft geben Sie an, wie ein Parameter an eine oder aus einer Prozedur übergeben wird. Die **Direction** -Eigenschaft bietet Lese-/Schreibzugriff. Dadurch können Sie Anbieter verwenden, die diese Informationen nicht zurückgeben, oder Sie können diese Informationen festlegen, wenn ADO den Anbieter nicht extra aufrufen soll, um Parameterinformationen abzurufen.

Nicht alle Anbieter können die Richtung von Parametern in ihren gespeicherten Prozeduren bestimmen. In diesen Fällen müssen Sie die **Direction** -Eigenschaft festlegen, bevor Sie die Abfrage ausführen.

