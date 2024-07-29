Tscheduler
Tasks Scheduler (Tscheduler) is a Python library that lets you schedule your Python code to be executed later, either just once or periodically. You can add new jobs or remove old ones on the fly as you please.

Among other things, Tscheduler can be used as a cross-platform, application specific replacement to platform specific schedulers, such as the cron daemon or the Windows task scheduler. Please note, however, that Tscheduler is not a daemon or service itself, nor does it come with any command line tools. It is primarily meant to be run inside existing applications. That said, Tscheduler does provide some building blocks for you to build a scheduler service or to run a dedicated scheduler process.

Tscheduler has three built-in scheduling systems you can use:

    Cron-style scheduling

    Interval-based execution (runs jobs on even intervals)

Tscheduler also integrates with several common Python frameworks, like:

    asyncio (PEP 3156)

    gevent

    Tornado

    Twisted

    Qt (using either PyQt , PySide6 , PySide2 or PySide)

There are third party solutions for integrating Tscheduler with other frameworks:

    Django

    Flask

    Fastapi
How to use
First we install the package from pypi.org
    pip install tscheduler
Second we call BackgroundScheduler from the package tscheduler
    from tscheduler.tscheduler import BackgroundScheduler
Python Example:
    from tscheduler.tscheduler import BackgroundScheduler

    def helio():
        print("hello")

    scheduler = BackgroundScheduler()
    scheduler.add_job(target=helio,trigger="interval",seconds=5)
    scheduler.start()
