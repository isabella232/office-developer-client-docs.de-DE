---
title: Connection.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 120ad21231187aa2cba21e1ef55c6f9d135b6934
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590081"
---
# <a name="connectionclose-method-dao"></a>Connection.Close-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **Connection**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* .Close

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Recordset**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Wenn Sie versuchen, ein **Connection**-Objekt zu schließen, für das noch **Recordset**-Objekte geöffnet sind, werden die **Recordset**-Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace**-Objekt zu schließen, für das noch **Connection**-Objekte geöffnet sind, werden diese **Connection**-Objekte geschlossen. Daraufhin werden deren **Recordset**-Objekte ebenfalls geschlossen.

Eine Alternative zur **Close**-Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

