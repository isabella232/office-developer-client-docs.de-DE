---
title: Implementieren von Objekten in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414942"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In C geschriebene Clientanwendungen und Dienstanbieter definieren #A0 durch Erstellen einer Datenstruktur und eines Arrays von geordneten Funktionszeigern, die als virtuelle Funktionstabelle oder vtable bezeichnet werden. Ein Zeiger auf die vtable muss das erste Element der Datenstruktur sein.
  
In der vtable selbst gibt es einen Zeiger für jede Methode in jeder Schnittstelle, die vom Objekt unterstützt wird. Die Reihenfolge der Zeiger muss der Reihenfolge der Methoden in der In der Mapidefs.h-Headerdatei veröffentlichten Schnittstellenspezifikation entsprechen. Jeder Funktionszeiger in der vtable wird auf die Adresse der tatsächlichen Implementierung der Methode festgelegt. In C++ richtet der Compiler die vtable automatisch ein. In C nicht. 
  
Die folgende Abbildung zeigt, wie dies funktioniert. Das Feld ganz links stellt einen Client dar, der ein Dienstanbieterobjekt verwenden muss. Über die Sitzung ruft der Client einen Zeiger auf das Objekt, **lpObject , ab.** Die vtable wird zuerst im Objekt angezeigt, gefolgt von privaten Daten und Methoden. Der vtable-Zeiger zeigt auf die tatsächliche vtable, die Zeiger auf jede Implementierung der Methoden in der Schnittstelle enthält. 
  
**Objektimplementierung**
  
![Objektimplementierung](media/amapi_42.gif "Objektimplementierung")
  
Das folgende Codebeispiel zeigt, wie ein C-Dienstanbieter ein einfaches Statusobjekt definieren kann. Das erste Element ist der #A0 Der Rest des Objekts besteht aus Datenm membern. 
  
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

Da es sich bei diesem Objekt um ein Statusobjekt handelt, enthält die vtable Zeiger auf Implementierungen der einzelnen Methoden in der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) sowie Zeiger auf Implementierungen der einzelnen Methoden in den Basisschnittstellen – **IUnknown** und **IMAPIProp**. Die Reihenfolge der Methoden in der vtable entspricht der angegebenen Reihenfolge, die in der Mapidefs.h-Headerdatei definiert ist.
  
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

In C geschriebene Clients und Dienstanbieter verwenden Objekte indirekt über die vtable und fügen einen Objektzeiger als ersten Parameter in jedem Aufruf hinzu. Jeder Aufruf einer MAPI-Schnittstellenmethode erfordert einen Zeiger auf das Objekt, das als erster Parameter aufgerufen wird. C++ definiert einen speziellen Zeiger, der zu diesem Zweck als **dieser** Zeiger bezeichnet wird. Der C++-Compiler fügt  den Zeiger implizit als ersten Parameter zu jedem Methodenaufruf hinzu. In C gibt es keinen solchen Zeiger. sie muss explizit hinzugefügt werden. 
  
Der folgende Code veranschaulicht, wie ein Client eine Instanz von MYSTATUSOBJECT aufrufen kann:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

