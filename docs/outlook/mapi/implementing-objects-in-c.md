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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310189"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In C geschriebene Client Anwendungen und Dienstanbieter definieren MAPI-Objekte, indem Sie eine Datenstruktur und ein Array von sortierten Funktionszeigern erstellen, die als virtuelle Funktionstabelle oder Vtable bezeichnet werden. Ein Zeiger auf die Vtable muss das erste Element der Datenstruktur sein.
  
In der vtable selbst gibt es einen Zeiger für jede Methode in jeder Schnittstelle, die vom Objekt unterstützt wird. Die Reihenfolge der Zeiger muss der Reihenfolge der Methoden in der Schnittstellenspezifikation entsprechen, die in der Headerdatei Mapidefs. h veröffentlicht ist. Jeder Funktionszeiger in der vtable wird auf die Adresse der tatsächlichen Implementierung der Methode festgelegt. In C++ richtet der Compiler automatisch die Vtable ein. In C ist dies nicht der Fall. 
  
Die folgende Abbildung zeigt, wie dies funktioniert. Das Feld ganz links steht für einen Client, der ein Dienstanbieterobjekt verwenden muss. Über die Sitzung erhält der Client einen Zeiger auf das Objekt **lpObject**. Die Vtable wird zuerst im-Objekt angezeigt, gefolgt von privaten Daten und Methoden. Der vtable-Zeiger verweist auf die tatsächliche Vtable, die Zeiger auf jede Implementierung der Methoden in der Schnittstelle enthält. 
  
**Objektimplementierung**
  
![Objekt Implementierung] (media/amapi_42.gif "Objekt Implementierung")
  
Im folgenden Codebeispiel wird veranschaulicht, wie ein C-Dienstanbieter ein einfaches Statusobjekt definieren kann. Das erste Element ist der vtable-Zeiger; der Rest des Objekts besteht aus Datenelementen. 
  
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

Da dieses Objekt ein Statusobjekt ist, enthält die vtable Zeiger auf Implementierungen der einzelnen Methoden in der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle sowie Zeiger auf Implementierungen der einzelnen Methoden in den Basisschnittstellen – **IUnknown **und **IMAPIProp**. Die Reihenfolge der Methoden in der vtable entspricht der angegebenen Reihenfolge, wie in der Headerdatei Mapidefs. h definiert.
  
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

In C geschriebene Clients und Dienstanbieter verwenden Objekte indirekt über die Vtable und fügen in jedem Aufruf einen Objektzeiger als ersten Parameter hinzu. Jeder Aufruf einer MAPI-Schnittstellenmethode erfordert einen Zeiger auf das Objekt, das als erster Parameter aufgerufen wird. C++ definiert einen speziellen Zeiger, der als **dieser** Zeiger bezeichnet wird. Der C++-Compiler fügt implizit den **this** -Zeiger als ersten Parameter für jeden Methodenaufruf hinzu. In C gibt es keinen solchen Zeiger; Sie muss explizit hinzugefügt werden. 
  
Der folgende Code veranschaulicht, wie ein Client einen Aufruf an eine Instanz von mySTATUSobject ausführen kann:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

