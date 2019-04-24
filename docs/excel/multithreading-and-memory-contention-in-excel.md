---
title: Multithreading und Speicher Konflikte in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in Excel, Arbeitsspeicher Konflikte in Excel, Funktionen [Excel 2007], Thread-sichere, threadsichere Funktionen [Excel 2007], Thread-lokaler Arbeitsspeicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301638"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading und Speicher Konflikte in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Versionen von Microsoft Excel vor Excel 2007 verwenden einen einzelnen Thread für alle Arbeitsblattberechnungen. Excel kann jedoch ab Excel 2007 für die Verwendung von 1 bis 1024 gleichzeitigen Threads für die Arbeitsblatt Berechnung konfiguriert werden. Bei einem Multi-Processor-oder Multi-Core-Computer entspricht die Standardanzahl von Threads der Anzahl von Prozessoren oder Kernen. Daher können threadsichere Zellen oder Zellen, die nur Funktionen enthalten, die threadsicher sind, gleichzeitigen Threads zugewiesen werden, vorbehaltlich der üblichen neuberechnungs Logik, die nach ihren Vorgänger Berechnungen berechnet werden muss.
  
## <a name="thread-safe-functions"></a>Thread sichere Funktionen

Die meisten der integrierten Arbeitsblattfunktionen, die in Excel 2007 beginnen, sind threadsicher. Sie können XLL-Funktionen auch als threadsicher schreiben und registrieren. Excel verwendet einen Thread (seinen Hauptthread), um alle Befehle, Thread unsichere Funktionen, **xlAuto** -Funktionen (außer [xlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12**) sowie com-und Visual Basic für Applikationen (VBA)-Funktionen aufzurufen.
  
Wenn eine XLL-Funktion eine **XLOPER** oder **XLOPER12** mit **xlbitDLLFree** -Satz zurückgibt, verwendet Excel den gleichen Thread, auf dem der Funktionsaufruf ausgeführt wurde, um **xlAutoFree** oder **xlAutoFree12**aufzurufen. Der Aufruf von **xlAutoFree** oder **xlAutoFree12** erfolgt vor dem nächsten Funktionsaufruf für diesen Thread. 
  
Für XLL-Entwickler gibt es Vorteile beim Erstellen von threadsicheren Funktionen:
  
- Sie ermöglichen Excel das Beste aus einem Computer mit mehreren Prozessoren oder Mehrprozessor Kernen.
    
- Sie eröffnen die Möglichkeit, Remoteserver wesentlich effizienter zu verwenden als mit einem einzigen Thread.
    
Angenommen, Sie verfügen über einen Computer mit einem Prozessor, der für die Verwendung von, sagen wir, *N* -Threads konfiguriert wurde. Angenommen, eine Arbeitsmappe wird ausgeführt, die eine hohe Anzahl von Aufrufen einer XLL-Funktion ausgibt, die wiederum eine Datenanforderung sendet oder eine Berechnung für einen Remoteserver oder-Cluster von Servern durchgeführt werden soll. Abhängig von der Topologie der Abhängigkeitsstruktur kann Excel die Funktion N-mal fast gleichzeitig aufrufen. Unter der Voraussetzung, dass der Server oder die Server ausreichend schnell oder parallel sind, kann die Neuberechnungszeit des Arbeitsblatts um den Faktor 1/N reduziert werden. 
  
Das Hauptproblem beim Schreiben von threadsicheren Funktionen ist das korrekte verarbeiten von Ressourcenkonflikten. Dies ist in der Regelspeicher Konflikte und kann in zwei Probleme unterteilt werden:
  
- Das Erstellen von Arbeitsspeicher, den Sie kennen, wird nur von diesem Thread verwendet.
    
- Sicherstellen, dass auf freigegebener Arbeitsspeicher über mehrere Threads sicher zugegriffen wird.
    
Das erste, was Sie beachten sollten, ist der Zugriff auf den Arbeitsspeicher in einer XLL für alle Threads, auf den nur über den aktuell ausgeführten Thread zugegriffen werden kann.
  
 **Zugänglich für alle Threads**
  
- Variablen, Strukturen und Klasseninstanzen, die außerhalb des Texts einer Funktion deklariert wurden.
    
- Statische Variablen, die innerhalb des Texts einer Funktion deklariert werden.
    
In diesen beiden Fällen wird der Speicherplatz im Speicherblock der DLL reserviert, der für diese DLL-Instanz erstellt wurde. Wenn eine andere Anwendungsinstanz die DLL lädt, erhält Sie eine eigene Kopie dieses Speichers, sodass keine Konflikte für diese Ressourcen von außerhalb dieser DLL-Instanz vorhanden sind.
  
 **Nur vom aktuellen Thread zugänglich**
  
- Automatische Variablen innerhalb des Funktionscodes (einschließlich der Funktionsargumente).
    
In diesem Fall wird der Speicher für jede Instanz des Funktionsaufrufs auf dem Stapel reserviert.
  
> [!NOTE]
> Der Bereich des dynamisch zugewiesenen Arbeitsspeichers hängt vom Bereich des Zeigers ab, der darauf zeigt: Wenn der Mauszeiger auf alle Threads zugreifen kann, ist auch der Arbeitsspeicher. Wenn der Zeiger eine automatische Variable in einer Funktion ist, ist der zugewiesene Arbeitsspeicher effektiv für diesen Thread privat. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Arbeitsspeicher, der von nur einem Thread zugänglich ist: Thread-lokaler Arbeitsspeicher

Da statische Variablen innerhalb des Texts einer Funktion für alle Threads zugänglich sind, sind die Funktionen, die Sie verwenden, eindeutig nicht threadsicher. Eine Instanz der Funktion in einem Thread könnte den Wert ändern, während eine andere Instanz in einem anderen Thread davon ausgeht, dass es sich um etwas vollständig anderes handelt. 
  
Es gibt zwei Gründe für das Deklarieren von statischen Variablen innerhalb einer Funktion:
  
1. Statische Daten bleiben von einem Aufruf zum nächsten erhalten.
    
2. Ein Zeiger auf statische Daten kann sicher von der Funktion zurückgegeben werden.
    
Im ersten Grund möchten Sie möglicherweise Daten beibehalten, die für alle Aufrufe der Funktion von Bedeutung sind: vielleicht ein einfacher Zähler, der bei jedem Aufruf der Funktion in einem Thread erhöht wird, oder eine Struktur, die Nutzungs-und Leistungsdaten von Eve sammelt. Anruf. Die Frage ist, wie die freigegebenen Daten oder die Datenstruktur geschützt werden. Am besten verwenden Sie den Abschnitt Critical Section, wie im nächsten Abschnitt erläutert wird.
  
Wenn die Daten nur für die Verwendung durch diesen Thread vorgesehen sind, was der Fall für den Grund 1 sein kann und bei Grund 2 immer der Fall ist, stellt sich die Frage, wie Arbeitsspeicher erstellt werden soll, der aber nur von diesem Thread aus zugänglich ist. Eine Lösung besteht darin, die TLS-API (Thread-Local Storage) zu verwenden.
  
Betrachten Sie beispielsweise eine Funktion, die einen Zeiger auf eine **XLOPER**zurückgibt.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Diese Funktion ist nicht threadsicher, da ein Thread die statische **XLOPER12** zurückgeben kann, während eine andere überschrieben wird. Die Wahrscheinlichkeit für dieses Ereignis ist noch größer, wenn die **XLOPER12** an **xlAutoFree12**übergeben werden muss. Eine Lösung besteht darin, eine **XLOPER12**zu reservieren, einen Zeiger darauf zurückzugeben und **xlAutoFree12** zu implementieren, damit der **XLOPER12** -Speicher selbst freigegeben wird. Dieser Ansatz wird in vielen der Beispiel Funktionen verwendet, die in der [Speicherverwaltung in Excel](memory-management-in-excel.md)angezeigt werden.
  
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

Dieser Ansatz ist einfacher zu implementieren als der im nächsten Abschnitt beschriebene Ansatz, der auf der TLS-API basiert, aber einige Nachteile hat. Zunächst muss Excel **xlAutoFree**/ **xlAutoFree12** aufrufen, unabhängig vom Typ des zurückgegebenen **XLOPER**/ -**XLOPER12**. Zweitens gibt es ein Problem beim Zurückgeben von **XLOPER**/ **XLOPER12**s, die der Rückgabewert eines Aufrufs an eine C-API-Rückruffunktion sind. Der **XLOPER**/ -**XLOPER12** kann auf Speicher verweisen, der von Excel freigegeben werden muss, aber die **XLOPER**/ -**XLOPER12** selbst muss auf die gleiche Weise freigegeben werden, wie Sie zugewiesen wurde. Wenn ein solches **XLOPER**/ -**XLOPER12** als Rückgabewert einer XLL-Arbeitsblattfunktion verwendet werden soll, gibt es keine einfache Möglichkeit, **xlAutoFree**/ **xlAutoFree12** darüber zu informieren, dass beide Zeiger auf die entsprechende Weise freigegeben werden müssen. (Sowohl die **xlbitXLFree** -als auch die **xlbitDLLFree** -Einstellung lösen das Problem nicht, da die Behandlung von **XLOPER/XLOPER12s** in Excel mit beiden Sätzen nicht definiert ist und möglicherweise von Version zu Version wechselt.) Um dieses Problem zu umgehen, kann die XLL Tiefe Kopien aller Excel-reservierten **XLOPER/XLOPER12s** , die es an das Arbeitsblatt zurückgibt. 
  
Eine Lösung, die diese Einschränkungen verhindert, ist das Auffüllen und Zurückgeben eines Thread-lokalen **XLOPER/XLOPER12**, ein Ansatz, der erfordert, dass **xlAutoFree/xlAutoFree12** den **XLOPER/XLOPER12-** Zeiger selbst nicht freilässt. 
  
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

Die nächste Frage ist, wie Sie den threadlokalen Arbeitsspeicher einrichten und abrufen, mit anderen Worten, wie Sie die Funktion **get_thread_local_xloper12** im vorherigen Beispiel implementieren. Dies erfolgt mithilfe der TLS-API (Local Storage). Der erste Schritt besteht darin, einen TLS-Index mithilfe von **TlsAlloc**abzurufen, der letztendlich mithilfe von **TlsFree**veröffentlicht werden muss. Beides wird am besten von **DllMain**aus ausgeführt.
  
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

Nachdem Sie den Index abgerufen haben, besteht der nächste Schritt im Zuweisen eines Speicherblocks für jeden Thread. Die [Windows-Entwicklungsdokumentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) empfiehlt dies jedes Mal, wenn die **DllMain** -Rückruffunktion mit einem **DLL_THREAD_ATTACH** -Ereignis aufgerufen wird und der Arbeitsspeicher auf jeder **DLL_THREAD_DETACH**freigegeben wird. Wenn Sie jedoch diese Ratschläge befolgen, würde Ihre DLL unnötige Arbeit für Threads ausführen, die nicht für die Neuberechnung verwendet werden. 
  
Stattdessen empfiehlt es sich, eine Allocate-on-First-use-Strategie zu verwenden. Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuweisen möchten. Für die vorherigen Beispiele, die **XLOPERs** oder **XLOPER12s**zurückgeben, genügt Folgendes, aber Sie können eine beliebige Struktur erstellen, die Ihren Anforderungen entspricht.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Die folgende Funktion Ruft einen Zeiger auf die Thread-lokale Instanz ab oder ordnet einen an, wenn es sich um den ersten Aufruf handelt.
  
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

Jetzt können Sie sehen, wie der Thread-lokale **XLOPER/XLOPER12** -Arbeitsspeicher abgerufen wird: zuerst rufen Sie einen Zeiger auf die Instanz von **TLS_data**des Threads ab und geben dann wie folgt einen Zeiger auf die darin enthaltene **XLOPER/XLOPER12** zurück. 
  
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

Die **mtr_safe_example_1** -und **mtr_safe_example_2** -Funktionen können bei der Verwendung von Excel als threadsichere Arbeitsblattfunktionen registriert werden. Die beiden Ansätze können jedoch nicht in einer XLL kombiniert werden. Ihre XLL kann nur eine Implementierung von **xlAutoFree** und **xlAutoFree12**exportieren, und jede Speicherstrategie erfordert eine andere Vorgehensweise. Bei **mtr_safe_example_1**muss der an **xlAutoFree/xlAutoFree12** übergebene Zeiger zusammen mit allen Daten freigegeben werden, auf die er verweist. Bei **mtr_safe_example_2**sollten nur die gezeigten Daten freigegeben werden.
  
Windows stellt auch eine Funktion **GetCurrentThreadId**bereit, die die eindeutige systemweite ID des aktuellen Threads zurückgibt. Dadurch erhält der Entwickler eine andere Möglichkeit, Code threadsicher zu machen, oder um sein Verhalten Thread spezifisch zu gestalten.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Arbeitsspeicher, der nur von mehreren Threads zugänglich ist: kritische Abschnitte

Sie sollten Lese-/Schreibzugriff schützen, auf den über kritische Abschnitte über mehrere Threads zugegriffen werden kann. Sie benötigen einen benannten kritischen Abschnitt für jeden zu schützenden Speicherblock. Sie können diese während des Aufrufs der **xlAutoOpen** -Funktion initialisieren und freigeben und Sie während des Aufrufs der **xlAutoClose** -Funktion auf NULL festlegen. Sie müssen dann jeden Zugriff auf den geschützten Block in einem Paar von Aufrufen an **EnterCriticalSection** und **LeaveCriticalSection**enthalten. Nur ein Thread ist jederzeit im kritischen Abschnitt zulässig. Nachfolgend finden Sie ein Beispiel für die Initialisierung, die uninitialisierung und die Verwendung eines Abschnittsnamens **g_csSharedTable**.
  
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

Eine weitere, vielleicht sicherere Möglichkeit zum Schutz eines Speicherblocks besteht darin, eine Klasse zu erstellen, die eine eigene **CRITICAL_SECTION** enthält und deren Konstruktor, Destruktor und Accessor-Methoden sich um ihre Verwendung kümmern. Dieser Ansatz hat den zusätzlichen Vorteil, Objekte zu schützen, die möglicherweise initialisiert werden, bevor **xlAutoOpen** ausgeführt wird, oder zu überleben, nachdem **xlAutoClose** aufgerufen wurde, aber Sie sollten vorsichtig sein, um zu viele kritische Abschnitte und das Betriebssystem zu erstellen. Aufwand. 
  
Wenn Sie über Code verfügen, der gleichzeitig auf mehr als einen geschützten Speicherblock zugreifen muss, müssen Sie die Reihenfolge, in der die kritischen Abschnitte eingegeben und beendet werden, sehr sorgfältig prüfen. Die folgenden beiden Funktionen können beispielsweise einen Deadlock verursachen.
  
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

Wenn die erste Funktion in einem Thread **g_csSharedTableA** eintritt, während der zweite in einem anderen Thread **g_csSharedTableB**eintritt, hängen beide Threads. Die richtige Vorgehensweise ist, wie folgt in eine konsistente Reihenfolge und Exit in umgekehrter Reihenfolge einzugeben.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Wenn möglich, ist es besser, den Zugriff auf verschiedene Blöcke zu isolieren, wie im folgenden dargestellt.
  
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

Wo es eine große Anzahl von Konflikten für eine freigegebene Ressource gibt, wie beispielsweise häufige Zugriffsanforderungen für kurze Zeit, sollten Sie erwägen, die Fähigkeit des kritischen Abschnitts zu verwenden. Dies ist eine Technik, die das warten auf die Ressource abnimmt. Zu diesem Zweck können Sie entweder **InitializeCriticalSectionAndSpinCount** beim Initialisieren des Abschnitts oder der **SetCriticalSectionSpinCount** nach der Initialisierung verwenden, um festzulegen, wie oft der Thread Schleifen soll, bevor darauf gewartet wird, dass Ressourcen verfügbar. Der Wartevorgang ist teuer, daher wird dies durch Drehen vermieden, wenn die Ressource in der Zwischenzeit freigegeben wird. Bei einem einzelnen Prozessorsystem wird die Anzahl der Drehungen effektiv ignoriert, aber Sie können Sie trotzdem angeben, ohne dass Sie Schaden anrichten müssen. Der Speicherheap-Manager verwendet eine Drehungs Anzahl von 4000. Weitere Informationen zur Verwendung kritischer Abschnitte finden Sie in der Windows SDK-Dokumentation. 
  
## <a name="see-also"></a>Siehe auch



[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

