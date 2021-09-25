---
title: Behandeln von MAPI-Eigenschaftsfehlern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1c4877dae64ae1890557a40723edbc66e07552b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580153"
---
# <a name="handling-mapi-property-errors"></a>Behandeln von MAPI-Eigenschaftsfehlern

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Anstatt vollst�ndige Fehler oder Erfolg melden die folgenden Methoden **IMAPIProp** partiellen Erfolg: 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps** partiellen Erfolg meldet, wenn mindestens eine der angeforderten Eigenschaften f�r ein Objekt abgerufen werden kann. **GetProps** gibt partiellen Erfolg an, indem die Warnung MAPI_W_ERRORS_RETURNED zur�ckgeben und Informationen zu den Eigenschaften nicht verf�gbar in den Wert-Array-Eigenschaft auf die durch den Parameter **lppPropArray**. Eine nicht verf�gbar-Eigenschaft Eintrag in diesem Array enth�lt PT_ERROR f�r den Eigenschaftentyp den **ulPropTag** Member und MAPI_E_NOT_FOUND oder einem anderen geeigneten Fehlerwert f�r den **Value** -Member. Beispielsweise platziert, wenn ein Client einen Ordner **GetProps** -Methode zum Abrufen von drei Eigenschaften aufruft, und die dritte nicht verf�gbar ist, der Nachricht Informationsdienst PT_ERROR in der dritten Eigenschaftstyp in Array der Wert-Eigenschaft und MAPI_E_NOT_FOUND im dritten-Eigenschaftenwert. 
  
Die anderen **IMAPIProp** Methoden Berichten partiellen Erfolg unterschiedlich. Diese Methoden Bericht partiellen Erfolg von wird S_OK zur�ckgegeben, und platzieren Fehlerinformationen in eine [SPropProblemArray](spropproblemarray.md) -Struktur. Im Gegensatz zu der Arrays der Eigenschaft Wert in **GetProps**, das Daten unabh�ngig davon, ob die Methode erfolgreich war oder nicht enth�lt, ist das Array-Eigenschaft Problem in diesen Methoden nur, wenn Fehler aufgetreten sind, und nur, wenn der Aufrufer Zinsen kennenzulernen Fehler registriert hat vorhanden. Anrufer m�ssen einen g�ltiger **SPropProblemArray** Zeiger f�r Fehlerinformationen registriert angeben. 
  
Wenn ein Fehlerwert von **SetProps**, **DeleteProps**, **CopyTo** oder **CopyProps** zur�ckgegeben wird, bedeutet dies Fehler anstelle von partiellen Erfolg. Das Array-Eigenschaft Problem ist gegebenenfalls ung�ltig. Clients sollte nicht versuchen, Zugriff auf Daten in der Struktur gehalten noch sollten sie versuchen, die Struktur selbst frei. Die entsprechende Antwort wird [IMAPIProp::GetLastError](imapiprop-getlasterror.md)aufzurufen. 
  
**GetLastError** ist vergleichbar mit der Funktion mit demselben Namen im Windows SDK bereitgestellt. Beide enthalten detailliertere Informationen zu einem Fehler als mit dem R�ckgabewert verf�gbar ist. Beide Zur�ckgeben von Informationen zu den vorherigen aufgetretenen Fehler. Der Unterschied besteht darin, dass die **GetLastError** Win32-Funktion einen Fehler vom aufrufenden meldet und die **IMAPIProp::GetLastError** -Methode ein Fehler generiert, die durch das aktuelle Objekt meldet. D. h., wenn ein Client **DeleteProps** f�r eine Nachricht und MAPI_E_NO_ACCESS aufruft wird um anzugeben, dass die Nachricht ist schreibgesch�tzt, **GetLastError** gibt Daten von der Nachricht zur�ckgegeben. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

