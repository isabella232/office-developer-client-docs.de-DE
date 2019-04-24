---
title: Recordset2. StillExecuting-Eigenschaft (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307217"
---
# <a name="recordset2stillexecuting-property-dao"></a>Recordset2. StillExecuting-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . StillExecuting

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mit der **StillExecuting**-Eigenschaft können Sie feststellen, ob die zuletzt aufgerufene asynchrone **Execute**- oder **OpenConnection**-Methode (d. h. eine Methode, die mit der **dbRunAsync**-Option aufgerufen wurde) abgeschlossen wurde. Solange die **StillExecuting**-Eigenschaft **True** ist, kann nicht auf zurückgegebene Objekte zugegriffen werden.

Wenn die **StillExecuting**-Eigenschaft im Anschluss an den **OpenConnection**-Aufruf, der das zugeordnete **Connection**-Objekt zurückgibt, **False** zurückgibt, kann auf das Objekt verwiesen werden. Solange **StillExecuting** noch **True** ist, kann nicht auf das Objekt verwiesen werden. Die **StillExecuting**-Eigenschaft kann in diesem Fall nur gelesen werden.

Mit der **[Cancel](connection-cancel-method-dao.md)** -Methode können Sie die Ausführung einer Aufgabe beenden.

