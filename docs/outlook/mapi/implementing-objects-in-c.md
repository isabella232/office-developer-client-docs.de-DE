---
title: Implementieren von Objekten in C#
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563947"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C#

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen und Dienstanbieter in C# geschriebenen definieren MAPI-Objekten, indem Sie erstellen eine Datenstruktur und ein Array von geordnete Funktionszeiger als virtuelle Funktion Tabellen oder Vtable bezeichnet. Ein Zeiger auf die Vtable muss das erste Element der Datenstruktur.
  
In der Vtable selbst wird einen Zeiger für jede Methode in jede Schnittstelle, die durch das Objekt unterstützt. Die Reihenfolge der Zeiger muss die Reihenfolge der Methoden in der Schnittstellenspezifikation veröffentlicht in der Headerdatei Mapidefs.h folgen. Jeder Funktionszeiger in der Vtable wird auf die Adresse der tatsächlichen Implementierung der-Methode festgelegt. In C++ richtet der Compiler automatisch die Vtable. In C ist es nicht. 
  
Die folgende Abbildung zeigt, wie dies funktioniert. Das Feld ganz links stellt einen Client, der eine dienstanbieterobjekts verwenden muss. In der Sitzung erhält der Client einen Zeiger auf das **LpObject**-Objekt. Die Vtable wird zuerst in das Objekt gefolgt von privaten Daten und Methoden angezeigt. Der Vtable-Zeiger verweist auf die tatsächliche Vtable, die Zeiger auf die einzelnen Implementierungen der Methoden in der Benutzeroberfläche der enthält. 
  
**Objektimplementierung**
  
![Objektimplementierung] (media/amapi_42.gif "Objektimplementierung")
  
Das folgende Codebeispiel zeigt, wie ein C#-Dienstanbieter ein einfaches Statusobjekt definieren kann. Das erste Element ist der Vtable-Zeiger; der Rest des Objekts Datenmember besteht. 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

Da dieses Objekt ein Statusobjekt ist, enthält die Vtable Zeigern für Implementierungen der einzelnen Methoden in der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle sowie Zeiger auf Implementierungen der einzelnen Methoden in die Basis Schnittstellen – **IUnknown **und **IMAPIProp**. Die Reihenfolge der Methoden in der Vtable entspricht die angegebene Reihenfolge in der Headerdatei Mapidefs.h definiert.
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

Clients-Dienstanbieter in C# geschriebenen Objekte indirekt über Vtable und verwenden einen Zeiger als der erste Parameter in jedem Aufruf hinzufügen. Alle Anrufe an einen MAPI-Schnittstelle-Methode erfordert einen Zeiger auf das Objekt als erster Parameter aufgerufen wird. C++ definiert einen speziellen Mauszeiger bekannt als **this** -Zeiger für diesen Zweck. Der C++ Compiler hinzugefügt **this** -Zeiger implizit als der erste Parameter auf jedem Methodenaufruf. In C# ist keine solche Zeiger; Es muss explizit hinzugefügt werden. 
  
Im folgenden Code wird veranschaulicht, wie ein Client einen Anruf mit einer Instanz des MYSTATUSOBJECT tätigen kann:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

