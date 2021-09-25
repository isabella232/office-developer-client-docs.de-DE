---
title: Multithreading und Speicherkonflikte in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading in excel,memory contention in Excel,functions [Excel 2007], threadsichere, threadsichere Funktionen [Excel 2007],threadlokaler Speicher [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 74f431357b74a117888eca847151a6145b2473e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621423"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading und Speicherkonflikte in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Versionen von Microsoft Excel vor Excel 2007 verwenden einen einzelnen Thread für alle Arbeitsblattberechnungen. Ab Excel 2007 können Excel jedoch für die Verwendung von gleichzeitigen Threads von 1 bis 1024 für die Arbeitsblattberechnung konfiguriert werden. Auf einem Computer mit mehreren Prozessoren oder Mitkernen entspricht die Standardanzahl von Threads der Anzahl der Prozessoren oder Kerne. Daher können threadsichere Zellen oder Zellen, die nur threadsichere Funktionen enthalten, gleichzeitigen Threads zugewiesen werden, die der üblichen Neuberechnungslogik unterliegen, die nach ihren Vorgängern berechnet werden muss.
  
## <a name="thread-safe-functions"></a>Thread-Safe Funktionen

Die meisten der integrierten Arbeitsblattfunktionen ab Excel 2007 sind threadsicher. Sie können XLL-Funktionen auch als threadsicher schreiben und registrieren. Excel verwendet einen Thread (den Hauptthread), um alle Befehle, threadunsicheren Funktionen, **xlAuto-Funktionen** (außer [xlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12)** sowie COM- und Visual Basic for Applications -Funktionen (VBA) aufzurufen.
  
Wenn eine XLL-Funktion **XLOPER** oder **XLOPER12** mit **xlbitDLLFree-Satz** zurückgibt, verwendet Excel denselben Thread, in dem der Funktionsaufruf ausgeführt wurde, um **xlAutoFree** oder **xlAutoFree12** aufzurufen. Der Aufruf von **xlAutoFree** oder **xlAutoFree12** erfolgt vor dem nächsten Funktionsaufruf für diesen Thread. 
  
Für XLL-Entwickler gibt es Vorteile beim Erstellen threadsicherer Funktionen:
  
- Sie ermöglichen Excel, einen Computer mit mehreren Prozessoren oder Mitkernen optimal zu nutzen.
    
- Sie bieten die Möglichkeit, Remoteserver viel effizienter zu verwenden, als dies mit einem einzigen Thread möglich ist.
    
Angenommen, Sie verfügen über einen Computer mit einem Einzelnen Prozessor, der für die Verwendung von z. B.  *N-Threads*  konfiguriert wurde. Angenommen, eine Kalkulationstabelle wird ausgeführt, die eine große Anzahl von Aufrufen an eine XLL-Funktion ausführt, die wiederum eine Anforderung für Daten oder für eine Berechnung an einen Remoteserver oder einen Servercluster sendet. Abhängig von der Topologie der Abhängigkeitsstruktur können Excel die Funktion fast gleichzeitig N-mal aufrufen. Vorausgesetzt, dass der Server oder die Server ausreichend schnell oder parallel sind, kann die Neuberechnungszeit der Kalkulationstabelle um den Faktor 1/N reduziert werden. 
  
Das hauptproblem beim Schreiben threadsicherer Funktionen ist die ordnungsgemäße Behandlung von Ressourcenkonflikten. Dies bedeutet in der Regel Speicherkonflikte und kann in zwei Probleme unterteilt werden:
  
- Wie Sie Arbeitsspeicher erstellen, von dem Sie wissen, dass er nur von diesem Thread verwendet wird.
    
- So stellen Sie sicher, dass mehrere Threads sicher auf gemeinsam genutzten Speicher zugreifen.
    
Beachten Sie zunächst, auf welchen Speicher in einer XLL von allen Threads zugegriffen werden kann und was nur vom derzeit ausgeführten Thread zugänglich ist.
  
 **Zugriff durch alle Threads**
  
- Variablen, Strukturen und Klasseninstanzen, die außerhalb des Textkörpers einer Funktion deklariert sind.
    
- Statische Variablen, die im Textkörper einer Funktion deklariert sind.
    
In diesen beiden Fällen wird Speicher im Speicherblock der DLL reserviert, der für diese Instanz der DLL erstellt wurde. Wenn eine andere Anwendungsinstanz die DLL lädt, erhält sie eine eigene Kopie dieses Speichers, sodass keine Konflikte für diese Ressourcen von außerhalb dieser Instanz der DLL vorhanden sind.
  
 **Nur über den aktuellen Thread zugänglich**
  
- Automatische Variablen innerhalb des Funktionscodes (einschließlich Funktionsargumenten).
    
In diesem Fall wird Speicher für jede Instanz des Funktionsaufrufs auf dem Stapel reserviert.
  
> [!NOTE]
> Der Bereich des dynamisch zugewiesenen Speichers hängt vom Bereich des Zeigers ab, der darauf zeigt: Wenn der Zeiger von allen Threads zugänglich ist, ist auch der Speicher verfügbar. Wenn es sich bei dem Zeiger um eine automatische Variable in einer Funktion handelt, ist der zugewiesene Speicher für diesen Thread effektiv privat. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Speicher, auf den nur ein Thread zugriffen kann: Thread-Local Arbeitsspeicher

Angesichts der Tatsache, dass statische Variablen im Textkörper einer Funktion für alle Threads zugänglich sind, sind funktionen, die sie verwenden, eindeutig nicht threadsicher. Eine Instanz der Funktion in einem Thread könnte den Wert ändern, während eine andere Instanz in einem anderen Thread davon ausgeht, dass es sich um eine völlig andere handelt. 
  
Es gibt zwei Gründe für das Deklarieren statischer Variablen innerhalb einer Funktion:
  
1. Statische Daten bleiben von einem Aufruf zum nächsten erhalten.
    
2. Ein Zeiger auf statische Daten kann von der Funktion sicher zurückgegeben werden.
    
Im ersten Fall möchten Sie möglicherweise Daten haben, die beibehalten werden und bedeutungsgemäß für alle Aufrufe der Funktion haben: vielleicht ein einfacher Zähler, der bei jedem Aufruf der Funktion in einem beliebigen Thread erhöht wird, oder eine Struktur, die Bei jedem Aufruf Nutzungs- und Leistungsdaten sammelt. Die Frage ist, wie die freigegebenen Daten oder die Datenstruktur geschützt werden. Dies geschieht am besten mithilfe eines kritischen Abschnitts, wie im nächsten Abschnitt erläutert.
  
Wenn die Daten nur für die Verwendung durch diesen Thread vorgesehen sind, was für Grund 1 der Fall sein kann und für Grund 2 immer der Fall ist, ist die Frage, wie Speicher erstellt wird, der beibehalten wird, aber nur über diesen Thread zugänglich ist. Eine Lösung besteht darin, die Thread-Local Storage (TLS)-API zu verwenden.
  
Betrachten Sie beispielsweise eine Funktion, die einen Zeiger auf einen **XLOPER** zurückgibt.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Diese Funktion ist nicht threadsicher, da ein Thread den statischen **XLOPER12** zurückgeben kann, während ein anderer ihn überschreibt. Die Wahrscheinlichkeit, dass dies geschieht, ist immer noch größer, wenn **xlOPER12** an **xlAutoFree12** übergeben werden muss. Eine Lösung besteht darin, **xlOPER12** zuzuweisen, einen Zeiger darauf zurückzugeben und **xlAutoFree12** zu implementieren, sodass der **XLOPER12-Speicher** selbst freigegeben wird. Dieser Ansatz wird in vielen der Beispielfunktionen verwendet, die in der [Speicherverwaltung in Excel](memory-management-in-excel.md)gezeigt werden.
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Dieser Ansatz ist einfacher zu implementieren als der im nächsten Abschnitt beschriebene Ansatz, der von der TLS-API abhängt, aber einige Nachteile hat. Zuerst müssen Excel **xlAutoFree** /  **xlAutoFree12** unabhängig vom Typ der zurückgegebenen **XLOPER** /  **XLOPER12** aufrufen. Zweitens gibt es ein Problem beim Zurückgeben von **XLOPER** /  **XLOPER12-Werten,** die den Rückgabewert eines Aufrufs einer C-API-Rückruffunktion darstellen. XlOPER  /  **XLOPER12** verweist möglicherweise auf Speicher, der von Excel freigegeben werden muss, aber der **XLOPER** /  **XLOPER12** selbst muss auf die gleiche Weise freigegeben werden, wie er zugewiesen wurde. Wenn eine solche **XLOPER** /  **XLOPER12** als Rückgabewert einer XLL-Arbeitsblattfunktion verwendet werden soll, gibt es keine einfache Möglichkeit, **xlAutoFree** /  **xlAutoFree12** darüber zu informieren, dass beide Zeiger auf die richtige Weise freigegeben werden müssen. (Das Festlegen von **xlbitXLFree** und **xlbitDLLFree** löst das Problem nicht, da die Behandlung von **XLOPER/XLOPER12s** in Excel mit beiden Einstellungen nicht definiert ist und von Version zu Version geändert werden kann.) Um dieses Problem zu umgehen, kann die XLL tiefe Kopien aller Excel **zugewiesenen XLOPER/XLOPER12s** erstellen, die sie an das Arbeitsblatt zurückgibt. 
  
Eine Lösung, die diese Einschränkungen vermeidet, ist das Auffüllen und Zurückgeben eines threadlokalen **XLOPER/XLOPER12**- ein Ansatz, der erfordert, dass **xlAutoFree/xlAutoFree12** den **XLOPER/XLOPER12-Zeiger** selbst nicht freigibt. 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Die nächste Frage ist, wie der threadlokale Speicher eingerichtet und abgerufen wird, mit anderen Worten, wie die Funktion **get_thread_local_xloper12** im vorherigen Beispiel implementiert wird. Dies erfolgt mithilfe der THREAD LOCAL Storage (TLS)-API. Der erste Schritt besteht darin, einen TLS-Index mithilfe von **TlsAlloc** abzurufen, der letztendlich mit **TlsFree** freigegeben werden muss. Beides ist am besten mit **dllMain** erreicht.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Nachdem Sie den Index erhalten haben, besteht der nächste Schritt darin, für jeden Thread einen Speicherblock zuzuweisen. In [der Windows-Entwicklungsdokumentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) wird empfohlen, dies jedes Mal zu tun, wenn die **DllMain-Rückruffunktion** mit einem **DLL_THREAD_ATTACH-Ereignis** aufgerufen wird, und den Speicher auf jedem **DLL_THREAD_DETACH** freizugeben. Wenn Sie diese Empfehlung befolgen, führt die DLL jedoch dazu, dass sie unnötige Arbeit für Threads ausführt, die nicht für die Neuberechnung verwendet werden. 
  
Stattdessen ist es besser, eine Strategie für die Zuweisung bei der ersten Verwendung zu verwenden. Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuordnen möchten. Für die vorherigen Beispiele, die **XLOPERs** oder **XLOPER12s** zurückgeben, reicht Folgendes aus, Sie können jedoch eine beliebige Struktur erstellen, die Ihren Anforderungen entspricht.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Die folgende Funktion ruft einen Zeiger auf die threadlokale Instanz ab oder weist eine zu, wenn dies der erste Aufruf ist.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Nun können Sie sehen, wie der **threadlokale XLOPER/XLOPER12-Speicher** abgerufen wird: Zuerst erhalten Sie einen Zeiger auf die Instanz des Threads **von TLS_data,** und dann geben Sie wie folgt einen Zeiger auf den darin enthaltenen **XLOPER/XLOPER12** zurück. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Die **Funktionen mtr_safe_example_1** und **mtr_safe_example_2** können als threadsichere Arbeitsblattfunktionen registriert werden, wenn Sie Excel ausführen. Sie können die beiden Ansätze jedoch nicht in einer XLL kombinieren. Ihre XLL kann nur eine Implementierung von **xlAutoFree** und **xlAutoFree12** exportieren, und jede Speicherstrategie erfordert einen anderen Ansatz. Bei **mtr_safe_example_1** muss der an **xlAutoFree/xlAutoFree12** übergebene Zeiger zusammen mit allen Daten, auf die er verweist, freigegeben werden. Bei **mtr_safe_example_2** sollten nur die Daten freigegeben werden, auf die verwiesen wird.
  
Windows stellt auch eine Funktion **"GetCurrentThreadId"** bereit, die die eindeutige systemweite ID des aktuellen Threads zurückgibt. Dadurch erhält der Entwickler eine andere Möglichkeit, codethreadsicher zu machen oder seinen Verhaltensthread spezifisch zu gestalten.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Nur von mehr als einem Thread zugänglicher Speicher: Wichtige Abschnitte

Sie sollten Lese-/Schreibzugriff auf Speicher schützen, auf den über kritische Abschnitte von mehreren Threads zugegriffen werden kann. Sie benötigen einen benannten kritischen Abschnitt für jeden Speicherblock, den Sie schützen möchten. Sie können diese während des Aufrufs der **xlAutoOpen-Funktion** initialisieren, freigeben und während des Aufrufs der **xlAutoClose-Funktion** auf NULL festlegen. Sie müssen dann jeden Zugriff auf den geschützten Block innerhalb eines Aufrufpaars von **EnterCriticalSection** und **LeaveCriticalSection** enthalten. Es ist immer nur ein Thread im kritischen Abschnitt zulässig. Hier sehen Sie ein Beispiel für die Initialisierung, Die Initialisierung und Die Verwendung eines Abschnitts mit dem Namen **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Eine weitere, vielleicht sicherere Möglichkeit zum Schutz eines Speicherblocks besteht darin, eine Klasse zu erstellen, die eine eigene **CRITICAL_SECTION** enthält und deren Konstruktor-, Destruktor- und Accessormethoden die Verwendung übernehmen. Dieser Ansatz bietet den zusätzlichen Vorteil, Objekte zu schützen, die vor der Ausführung von **xlAutoOpen** initialisiert werden können, oder nach dem Aufruf von **xlAutoClose** erhalten bleiben. Sie sollten jedoch vorsichtig sein, wenn Sie zu viele kritische Abschnitte und den damit verbundenen Betriebssystemmehraufwand erstellen. 
  
Wenn Sie über Code verfügen, der gleichzeitig Zugriff auf mehrere Geschützte Speicherblocks benötigt, müssen Sie die Reihenfolge, in der die kritischen Abschnitte eingegeben und beendet werden, sehr sorgfältig abwägen. Die folgenden beiden Funktionen könnten z. B. einen Deadlock erzeugen.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Wenn die erste Funktion in einem Thread **g_csSharedTableA** eingibt, während der zweite in einem anderen Thread **g_csSharedTableB** wechselt, hängen beide Threads hängen. Der richtige Ansatz besteht darin, wie folgt in einer konsistenten Reihenfolge einzugeben und in umgekehrter Reihenfolge zu beenden.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Wenn möglich, ist es aus Sicht der Thread-Zusammenarbeit besser, den Zugriff auf unterschiedliche Blöcke zu isolieren, wie hier gezeigt.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Wenn es viele Konflikte für eine freigegebene Ressource gibt, z. B. häufige Zugriffsanfragen mit kurzer Dauer, sollten Sie erwägen, die Drehungsfähigkeit des kritischen Abschnitts zu verwenden. Dies ist eine Technik, die das Warten auf die Ressource weniger prozessorintensiv macht. Zu diesem Zweck können Sie entweder **InitializeCriticalSectionAndSpinCount** beim Initialisieren des Abschnitts oder **SetCriticalSectionSpinCount** nach der Initialisierung verwenden, um festzulegen, wie oft der Thread durchlaufen wird, bevor darauf gewartet wird, dass Ressourcen verfügbar werden. Der Wartevorgang ist teuer, daher wird dies beim Drehen vermieden, wenn die Ressource in der Zwischenzeit freigegeben wird. Bei einem einzelnen Prozessorsystem wird die Drehungsanzahl effektiv ignoriert, Sie können sie aber trotzdem angeben, ohne schaden zu müssen. Der Speicher-Heap-Manager verwendet eine Drehungsanzahl von 4000. Weitere Informationen zur Verwendung wichtiger Abschnitte finden Sie in der Windows SDK-Dokumentation. 
  
## <a name="see-also"></a>Siehe auch



[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

