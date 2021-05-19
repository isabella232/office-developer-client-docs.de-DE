---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334961"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Clientcomputer und stellt mapi32.dll mit der MAPI-Stubbibliothek mapistub.dll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |mapistub.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Rückgabewerte

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Nicht-Null-Wert.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert null. Rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)** auf, um erweiterte Fehlerinformationen zu erhalten. 
  
## <a name="remarks"></a>Hinweise

 **FixMAPI** ersetzt nicht die aktuelle mapi32.dll, wenn die Datei als schreibgeschützt gekennzeichnet ist. 
  
 **FixMAPI** ersetzt nicht die aktuelle mapi32.dll, Microsoft Exchange Server auf dem Computer installiert ist. 
  
Wenn **FixMAPI** eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Computer erstellt, weist sie der Sicherungskopie einen anderen Namen zu als "mapi32.dll". Anschließend werden nachfolgende Aufrufe, die für diese Assembly vorgesehen sind, an die Sicherungskopie weiter. 
  
## <a name="see-also"></a>Siehe auch



[KB 256946: Sie erhalten eine Fehlermeldung zum Programmkonflikt, wenn Sie Outlook 2000 starten](https://support.microsoft.com/kb/256946)
  
[KB 228457: Beschreibung des Fixmapi.exe, das in Internet Explorer 5 enthalten ist](https://support.microsoft.com/kb/228457)

