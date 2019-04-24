nullable/core Reference
==============================================================================

The following are the references for nullable/core.



Types
=====



Audience
---------------------------------------------------------

    .. code:: nim

        Audience* = enum
          ops,
          admin,
          user,
          public


    *source line: 28*

    Distribution limits for news of the hint.
    
    ops
      only seen by those with server/system maintainer clearance
    
    admin
      only seen by end-users with admin clearance (and ops)
    
    user
      only seen by regular users (and admin and ops)
    
    public
      the whole world (no restrictions)


Hint
---------------------------------------------------------

    .. code:: nim

        Hint* = object
          msg*: string           # defaults to ""
          level*: Level          # defaults to 'lvlAll'
          judgement*: Judgement  # defaults to 'info'
          audience*: Audience    # defaults to 'ops'


    *source line: 56*



Judgement
---------------------------------------------------------

    .. code:: nim

        Judgement* = enum
          info,
          success,
          warning,
          danger


    *source line: 7*

    Category of judgement for the hint.
    
    info
        neutral (but ok if forced to judge)
    
    success
        ok
    
    warning
        ok; but with reservations
    
    danger
        not ok
    
    These categories are inspired by the Bootstrap framework
    (https://getbootstrap.com/)


NState
---------------------------------------------------------

    .. code:: nim

        NState* = enum
          state_valued,
          state_nulled,
          state_errored


    *source line: 48*



NullClass
---------------------------------------------------------

    .. code:: nim

        NullClass* = object
          exists: bool          # note: this field is not actually used.


    *source line: 54*










Table Of Contents
=================

1. `Introduction to nullable <index.rst>`__
2. Appendices

    A. `nullable Reference <nullable-ref.rst>`__
    B. `nullable/nint General Documentation <nullable-nint-gen.rst>`__
    C. `nullable/nint Reference <nullable-nint-ref.rst>`__
    D. `nullable/core General Documentation <nullable-core-gen.rst>`__
    E. `nullable/core Reference <nullable-core-ref.rst>`__