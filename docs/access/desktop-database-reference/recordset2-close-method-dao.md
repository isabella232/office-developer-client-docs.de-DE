---
title: Recordset2.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f20c10ac6bb6fc313ffecb56b0d2852c3b488c26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474701"
---
# <a name="recordset2close-method-dao"></a>Recordset2.Close Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Schließt ein geöffnetes **Recordset** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Schließen Sie

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Recordset** -Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Wenn Sie versuchen, ein **Connection** -Objekt zu schließen, für das noch **Recordset** -Objekte geöffnet sind, werden die **Recordset** -Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace** -Objekt zu schließen, für das noch **Connection** -Objekte geöffnet sind, werden diese **Connection** -Objekte geschlossen. Daraufhin werden deren **Recordset** -Objekte ebenfalls geschlossen.

Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).

