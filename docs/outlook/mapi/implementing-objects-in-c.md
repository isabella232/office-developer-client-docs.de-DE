---
title: Implementieren von Objekten in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 821e59dc006b334383cad6367e19359d0f6006fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556448"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen und Dienstanbieter, die in C geschrieben wurden, definieren MAPI-Objekte, indem sie eine Datenstruktur und ein Array sortierter Funktionszeiger erstellen, die als virtuelle Funktionstabelle oder vtable bezeichnet werden. Ein Zeiger auf die vtable muss das erste Element der Datenstruktur sein.
  
In der vtable selbst gibt es einen Zeiger für jede Methode in jeder Schnittstelle, die vom Objekt unterstützt wird. Die Reihenfolge der Zeiger muss der Reihenfolge der Methoden in der in der Headerdatei Mapidefs.h veröffentlichten Schnittstellenspezifikation entsprechen. Jeder Funktionszeiger in der vtable wird auf die Adresse der tatsächlichen Implementierung der Methode festgelegt. In C++ richtet der Compiler die vtable automatisch ein. In C ist dies nicht der Typ. 
  
Die folgende Abbildung zeigt, wie dies funktioniert. Das Feld ganz links stellt einen Client dar, der ein Dienstanbieterobjekt verwenden muss. Während der Sitzung ruft der Client einen Zeiger auf das Objekt **lpObject** ab. Die vtable wird zuerst im Objekt angezeigt, gefolgt von privaten Daten und Methoden. Der vtable-Zeiger zeigt auf die tatsächliche vtable, die Zeiger auf jede Implementierung der Methoden in der Schnittstelle enthält. 
  
**Objektimplementierung**
  
![Objektimplementierung](media/amapi_42.gif "Objektimplementierung")
  
Das folgende Codebeispiel zeigt, wie ein C-Dienstanbieter ein einfaches Statusobjekt definieren kann. Das erste Element ist der vtable-Zeiger. Der Rest des Objekts besteht aus Datenmembern. 
  
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

Da dieses Objekt ein Statusobjekt ist, enthält die vtable Zeiger auf Implementierungen der einzelnen Methoden in der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) sowie Zeiger auf Implementierungen der einzelnen Methoden in den Basisschnittstellen - **IUnknown** und **IMAPIProp**. Die Reihenfolge der Methoden in der vtable stimmt mit der angegebenen Reihenfolge überein, die in der Headerdatei Mapidefs.h definiert ist.
  
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

In C geschriebene Clients und Dienstanbieter verwenden Objekte indirekt über die vtable und fügen als ersten Parameter in jedem Aufruf einen Objektzeiger hinzu. Jeder Aufruf einer MAPI-Schnittstellenmethode erfordert einen Zeiger auf das Objekt, das als erster Parameter aufgerufen wird. C++ definiert einen speziellen Zeiger, der als **dieser** Zeiger für diesen Zweck bezeichnet wird. Der C++-Compiler fügt **diesen** Zeiger implizit als ersten Parameter zu jedem Methodenaufruf hinzu. In C gibt es keinen solchen Zeiger; sie muss explizit hinzugefügt werden. 
  
Der folgende Code veranschaulicht, wie ein Client eine Instanz von MYSTATUSOBJECT aufrufen kann:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

