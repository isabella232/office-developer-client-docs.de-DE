---
title: Recordset2. Schließ-Methode (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307385"
---
# <a name="recordset2close-method-dao"></a>Recordset2. Schließ-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **Recordset**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Schließen

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Recordset**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Wenn Sie versuchen, ein **Connection**-Objekt zu schließen, für das noch **Recordset**-Objekte geöffnet sind, werden die **Recordset**-Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace**-Objekt zu schließen, für das noch **Connection**-Objekte geöffnet sind, werden diese **Connection**-Objekte geschlossen. Daraufhin werden deren **Recordset**-Objekte ebenfalls geschlossen.

Eine Alternative zur **Schließ** -Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

