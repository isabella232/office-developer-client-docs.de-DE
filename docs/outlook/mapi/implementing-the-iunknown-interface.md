---
title: Implementieren der IUnknown-Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310045"
---
# <a name="implementing-the-iunknown-interface"></a>Implementieren der IUnknown-Schnittstelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle, die in jedem MAPI-Objekt implementiert sind, unterstützen die Kommunikation zwischen Objekten und die Objektverwaltung. 
  
 **IUnknown** verfügt über drei Methoden: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)und [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** ermöglicht es einem Objekt, zu bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt. Mit **QueryInterface**können zwei Objekte, die keine Vorkenntnisse der Funktionalität des jeweils anderen besitzen, interagieren. Wenn das Objekt, das **QueryInterface** implementiert, die fragliche Schnittstelle unterstützt, wird ein Zeiger auf die Implementierung der Schnittstelle zurückgegeben. Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, wird der MAPI_E_INTERFACE_NOT_SUPPORTED-Wert zurückgegeben. 
  
Wenn **QueryInterface** einen angeforderten Schnittstellenzeiger zurückgibt, muss auch der Verweiszähler des neuen Objekts erhöht werden. Der Verweiszähler eines Objekts ist ein numerischer Wert, der zum Verwalten der Lebensdauer des Objekts verwendet wird. Wenn der Verweiszähler größer als 1 ist, kann der Arbeitsspeicher des Objekts nicht freigegeben werden, da er aktiv verwendet wird. Nur wenn der Verweiszähler auf 0 sinkt, kann das Objekt sicher freigegeben werden. 
  
Die anderen beiden **IUnknown** -Methoden **AddRef** und **Release**verwalten den Verweiszähler. **AddRef** inkrementiert den Verweiszähler, während die **Freigabe** ihn dekrementiert. Alle Methoden oder API-Funktionen, die Schnittstellenzeiger wie **QueryInterface**zurückgeben, müssen **AddRef** aufrufen, um den Verweiszähler zu erhöhen. Alle Implementierungen von Methoden, die Schnittstellenzeiger empfangen, müssen die **Freigabe** aufrufen, um die Anzahl zu verringern, wenn der Zeiger nicht mehr benötigt wird. **Release** prüft einen vorhandenen Verweiszähler, der den der Schnittstelle zugeordneten Arbeitsspeicher nur freigibt, wenn die Anzahl 0 ist. 
  
> [!NOTE]
> Da **AddRef** und **Release** keine genauen Werte zurückgeben müssen, dürfen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um zu bestimmen, ob ein Objekt noch gültig ist oder zerstört wurde. 
  
## <a name="see-also"></a>Siehe auch



[Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

